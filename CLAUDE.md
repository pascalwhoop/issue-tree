# Issue Tree - Project Guidance

## Project Overview

**Issue Tree** is a recursive problem-solving framework that uses Claude Code to decompose complex
problems into hierarchical trees of sub-problems.

### Key Concepts

-   Each problem node can either **decompose** into sub-problems or **solve** directly
-   Agents operate with strict information boundaries (can only see their node, ancestors, and
    children - NOT siblings)
-   Solutions bubble up from leaf nodes through synthesis

## Structure

```
issue-tree/
├── .claude/
│   └── skills/
│       ├── init-problem-tree/  # Initialize new problem trees
│       └── solve-node/          # Core recursive solver
├── german-gov-os-decision/      # Example problem tree
├── README.md                    # Full documentation
└── CLAUDE.md                    # This file
```

## Development Workflow

### Creating New Problem Trees

1. Use `/init-problem-tree` skill to set up a new problem
2. Navigate to the problem directory
3. Run the solver: `/solve-node skill"`

### Modifying Skills

Skills are in `.claude/skills/`. Key files:

-   `solve-node/SKILL.md`: Core recursive logic
-   `init-problem-tree/SKILL.md`: Initialization logic

When modifying, maintain:

-   Information access restrictions
-   Clear decompose vs solve decision criteria
-   Proper file structure conventions

### Testing

Test with simple problems first:

-   2-level trees (root + direct children that solve)
-   Then progress to more complex multi-level trees

Monitor:

-   STATUS.md files for progress
-   ANALYSIS.md for agent reasoning
-   SOLUTION.md for results

## Coding Standards

### File Naming

-   Use lowercase with hyphens for directories: `cost-analysis/`
-   Required files: `PROBLEM.md`, `STATUS.md`
-   Generated files: `ANALYSIS.md`, `SOLUTION.md`

### Markdown Structure

Each markdown file should have clear sections with `##` headers.

### Status Values

-   `pending`: Not started
-   `decomposed`: Sub-problems created
-   `solving`: Currently working
-   `solved`: Complete

## Information Access Rules

**CRITICAL**: When working as a solve-node agent:

✅ **Allowed**:

-   Your current node files
-   Parent/ancestor PROBLEM.md files (for context)
-   Your children in subproblems/

❌ **Forbidden**:

-   Sibling nodes at your level
-   Unrelated branches
-   Cousin nodes

This ensures independent exploration without contamination.

## Common Tasks

### Add a new skill

```bash
mkdir .claude/skills/new-skill
# Create SKILL.md with frontmatter and instructions
```

### Manually check tree progress

```bash
find . -name "STATUS.md" -exec grep -H "Status:" {} \;
```

### View all solutions in tree

```bash
find . -name "SOLUTION.md" -exec echo "=== {} ===" \; -exec cat {} \;
```

## Resources

-   Full documentation: `README.md`
-   Skills documentation: [Claude Code Skills Guide](https://code.claude.com/docs/en/skills.md)
-   Example problem tree: `german-gov-os-decision/`

## Working with This Project

When you're asked to work on this project, remember:

1. **If initializing a new problem**: Use or reference the `/init-problem-tree` skill
2. **If solving a problem node**: Use the `/solve-node` skill with information boundaries enforced
3. **If modifying the system**: Update skills in `.claude/skills/` and maintain the recursive
   structure
4. **If testing**: Start with the example `german-gov-os-decision/` tree

Always respect the information access boundaries when working as a solver agent!
