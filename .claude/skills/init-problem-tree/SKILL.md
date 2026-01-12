---
name: init-problem-tree
description:
    Initialize a new problem tree for recursive problem solving. Use when the user wants to set up a
    new problem to solve using the tree decomposition approach.
---

# Initialize Problem Tree

This skill helps you set up a new problem tree for recursive problem solving.

## Instructions

When a user wants to start a new problem tree:

1. **Clarify the problem**: Make sure you understand the root problem/question clearly. Ask for
   clarification if needed.

2. **Choose/create the root directory**:

    - Ask the user where they want to create the problem tree, or suggest a name based on the
      problem
    - Create the directory: `mkdir -p issues/problem-name`

3. **Create the root PROBLEM.md**:

    ```markdown
    # Problem: [Title]

    ## Question

    [The main question or problem to solve]

    ## Context

    [Why this problem matters] [Any relevant background information] [Constraints or requirements]

    ## Success Criteria

    [What constitutes a good solution] [How will we know when this is answered]

    ## Notes

    [Any additional information]
    ```

4. **Create STATUS.md**:

    ```markdown
    # Status: pending

    Created: [current date/time] Last updated: [current date/time]
    ```

5. **Create README.md** (for navigation):

    ```markdown
    # Problem Tree: [Problem Name]

    ## Root Problem

    [Brief description]

    ## Structure

    This is a recursive problem-solving tree. Each node can either:

    -   Be decomposed into sub-problems (creates subproblems/ folder)
    -   Be solved directly (creates SOLUTION.md)

    ## Files

    -   `PROBLEM.md` - The problem/question at this node
    -   `STATUS.md` - Current status (pending/decomposed/solving/solved)
    -   `ANALYSIS.md` - Analysis and reasoning (created by solver)
    -   `SOLUTION.md` - The answer (created when solved)
    -   `subproblems/` - Child problem nodes (if decomposed)

    ## Usage

    To work on this problem tree:
    ```

    cd issues/problem-name

    # Then invoke the solve-node skill or run:

    # /solve-node

    ```

    ## Current Status
    See STATUS.md for current state.
    ```

6. **Inform the user**:
    - Show them the structure you created
    - Explain that they can now run `/solve-node` or invoke the solve-node skill to start solving
    - Optionally offer to start the solving process immediately

## Example

User: "I want to solve whether the German government should use Linux or Windows"

You should:

1. Create `issues/german-gov-os-decision/`
2. Create PROBLEM.md with the question clearly stated
3. Create STATUS.md set to "pending"
4. Create README.md with overview
5. Tell the user the tree is ready and offer to start solving

## Tips

-   Make directory names descriptive but concise (use lowercase and hyphens)
-   Make sure the problem is stated clearly and specifically in PROBLEM.md
-   Include any constraints or context the user provides
-   Set realistic success criteria
