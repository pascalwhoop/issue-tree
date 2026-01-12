# Issue Tree - Recursive Problem Solving System

A recursive problem-solving framework that decomposes complex problems into hierarchical trees of sub-problems, each solved independently by autonomous Claude agents.

## Concept

The Issue Tree system allows you to solve complex problems by:

1. **Decomposition**: Breaking down a complex problem into smaller, manageable sub-problems
2. **Independent Solving**: Each sub-problem is solved by an independent agent with limited information access
3. **Synthesis**: Solutions bubble up from leaf nodes to parent nodes until the root problem is solved

### Key Principles

- **Recursive Structure**: Each node can either decompose further or solve directly
- **Information Boundaries**: Agents can only see their node, ancestors (for context), and children (for synthesis)
- **No Sibling Access**: Parallel branches remain independent to prevent contamination
- **Autonomous Agents**: Each node is handled by a separate Claude instance with the same recursive logic

## Architecture

### File Structure

Each problem node follows this structure:

```
problem-node/
├── PROBLEM.md       # The question/problem at this node
├── STATUS.md        # Current status: pending/decomposed/solving/solved
├── ANALYSIS.md      # Agent's reasoning and approach
├── SOLUTION.md      # The answer (when solved)
└── subproblems/     # Child nodes (if decomposed)
    ├── subproblem-1/
    ├── subproblem-2/
    └── ...
```

### Information Flow

```
root/
├── PROBLEM.md ────────┐
└── subproblems/       │
    ├── cost-analysis/ │ (can read parent)
    │   ├── PROBLEM.md │
    │   └── ...        │
    │                  │
    ├── security/      │ (can read parent)
    │   ├── PROBLEM.md │
    │   └── ...        │
    │                  │
    └── compatibility/ │ (can read parent)
        └── ...        │

Note: cost-analysis CANNOT see security/ or compatibility/ (siblings)
```

## Skills

The system provides two Claude Code skills:

### 1. `/init-problem-tree`

Initialize a new problem tree.

**Usage:**
```bash
# In your workspace
claude

# Then tell Claude:
"Initialize a problem tree for: Should the German government use Linux or Windows?"
```

This creates the root problem structure.

### 2. `/solve-node`

The core recursive solver. When invoked at a node, it will:

1. Read and understand the problem
2. Decide whether to DECOMPOSE or SOLVE
3. If DECOMPOSE:
   - Create sub-problem folders
   - Write PROBLEM.md for each
   - Invoke child Claude agents for each sub-problem
   - Wait for solutions and synthesize
4. If SOLVE:
   - Research/experiment to find the answer
   - Write SOLUTION.md with findings

**Usage:**
```bash
# Navigate to a problem node
cd german-gov-os-decision

# Invoke the solver
claude -p "Use the /solve-node skill to solve the problem in the current directory"
```

## How It Works

### Step-by-Step Example

Let's say you want to solve: "Should the German government use Linux or Windows?"

1. **Initialize the tree:**
   ```bash
   claude
   # Tell Claude: "Use /init-problem-tree for: Should German gov use Linux or Windows?"
   ```

2. **Start solving:**
   ```bash
   cd german-gov-os-decision
   claude -p "Use /solve-node skill"
   ```

3. **Agent at root decides to DECOMPOSE:**
   - Creates subproblems: cost-analysis, security-comparison, compatibility, support-ecosystem, case-studies
   - Writes PROBLEM.md for each
   - Invokes 5 child Claude agents (one per sub-problem)

4. **Each child agent runs independently:**
   - cost-analysis agent: Might SOLVE directly by researching costs
   - security-comparison agent: Might SOLVE directly by comparing security features
   - case-studies agent: Might DECOMPOSE into specific country case studies (Munich, France, etc.)

5. **Solutions bubble up:**
   - Leaf nodes solve and write SOLUTION.md
   - Parent nodes read child SOLUTION.md files
   - Parent synthesizes into its own SOLUTION.md
   - Process continues up to root

6. **Final result:**
   - Root SOLUTION.md contains the comprehensive answer
   - All supporting analysis is in the tree structure

### Nesting and Recursion

- Claude Code has a 1-level nesting limit for subagents
- We bypass this by invoking the `claude` binary directly via Bash
- Each invocation is independent, allowing unlimited nesting depth
- The system supports up to 4+ levels of decomposition

### Parallelization

Agents at the same level run in parallel:

```bash
cd subproblems/problem-1 && claude -p "Use /solve-node" &
cd subproblems/problem-2 && claude -p "Use /solve-node" &
cd subproblems/problem-3 && claude -p "Use /solve-node" &
wait
```

This speeds up solving significantly.

## Design Decisions

### Why Information Boundaries?

Restricting agents to only see their node, ancestors, and children (not siblings) ensures:

- **Independent exploration**: Each branch explores without bias from parallel branches
- **Diverse approaches**: Different agents may try different methods for similar problems
- **Clean synthesis**: Parent knows how to combine child solutions without cross-contamination
- **Scalability**: Agents don't need to load irrelevant parts of the tree

### When to DECOMPOSE vs SOLVE?

The agent decides based on:

**DECOMPOSE when:**
- Problem requires multiple distinct sub-questions
- Different aspects need different types of research
- Problem is broad with natural subdivisions
- Cannot answer without constituent questions

**SOLVE when:**
- Can research/experiment directly
- Problem is specific and focused
- Clear methodology exists
- Further breakdown adds no value

## Example Problem Trees

### Simple (2 levels):
```
"What's the market cap of AI companies?"
├── us-ai-companies/     [SOLVE: direct research]
├── european-ai-companies/ [SOLVE: direct research]
└── asian-ai-companies/  [SOLVE: direct research]
```

### Complex (4 levels):
```
"Should German gov use Linux or Windows?"
├── cost-analysis/
│   ├── licensing-costs/        [SOLVE]
│   ├── migration-costs/        [SOLVE]
│   └── ongoing-maintenance/    [SOLVE]
├── security-comparison/        [SOLVE]
├── compatibility/
│   ├── existing-systems/       [SOLVE]
│   └── vendor-software/        [SOLVE]
├── support-ecosystem/          [SOLVE]
└── case-studies/
    ├── munich-limux/           [SOLVE]
    ├── france-gendarmerie/     [SOLVE]
    └── barcelona-analysis/     [SOLVE]
```

## Usage Tips

1. **Start broad**: Initialize with the high-level problem
2. **Trust the process**: Let agents decide how to decompose
3. **Review incrementally**: Check STATUS.md files to see progress
4. **Read solutions bottom-up**: Start at leaf nodes, work to root
5. **Iterate if needed**: If a solution is unsatisfactory, you can re-run that node

## Technical Details

### Skills Location

Skills are in `.claude/skills/`:
- `.claude/skills/init-problem-tree/SKILL.md`
- `.claude/skills/solve-node/SKILL.md`

### Status Values

- `pending`: Not yet started
- `decomposed`: Sub-problems created, waiting for child solutions
- `solving`: Currently researching/working
- `solved`: Solution complete

### Required Files

Each node MUST have:
- `PROBLEM.md`: What needs to be answered
- `STATUS.md`: Current state

Generated by agents:
- `ANALYSIS.md`: Agent's reasoning
- `SOLUTION.md`: The answer
- `subproblems/`: Child nodes (if decomposed)

## Limitations

- Requires Claude Code CLI
- Each agent invocation uses API credits
- Large trees can take time (though parallelized)
- Depth limited by practical considerations (4-5 levels recommended max)
- No automatic retrying of failed nodes (must manually re-run)

## Future Enhancements

Possible improvements:
- Progress dashboard showing tree status
- Automatic retry logic for failed nodes
- Cost estimation before running
- Visualization of the problem tree
- Confidence scoring aggregation
- Conflict detection between branch solutions

## Getting Started

1. Ensure Claude Code is installed
2. Navigate to this directory
3. Initialize a problem tree: `claude` then use `/init-problem-tree`
4. Start solving: `cd <problem-dir> && claude -p "Use /solve-node"`
5. Monitor progress by checking STATUS.md files
6. Read SOLUTION.md files when complete

## Example Session

```bash
# Start Claude
claude

# In Claude, initialize:
> Initialize a problem tree for: What programming language should we use for our web backend?

# Claude creates: web-backend-language/

# Start solving:
cd web-backend-language
claude -p "Use the /solve-node skill to solve this problem"

# Claude decomposes into:
# - performance-requirements/
# - ecosystem-and-libraries/
# - team-expertise/
# - scalability-needs/
# - cost-considerations/

# Each sub-problem is solved independently
# Final SOLUTION.md synthesizes all findings

# Read the result:
cat SOLUTION.md
```

## License

MIT

## Contributing

This is a prototype system. Feel free to extend and improve!
