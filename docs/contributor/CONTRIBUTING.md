# Contributing

The `Openlore Sparks` project will be an **Open Source Project**.

## Branch Management

```
   main           Main branch.
    ┣━ dev        Development branch.
    ┃   ┣━ ftr    Feature branch.
    ┃   ┣━ fix    Fix branch, for bugs or otherwise, not adding functionality.
    ┃   ┗━ rel    Release branch.
    ┗━ hot        Urgent production fix branch.
```

Except for main, all branches have a three-letter name. The purpose of a fixed three-letter length is to ensure each section of the name aligns perfectly in a vertical list for easy visual scanning.

## Branch name sections

**Branch name**  
The first section, the branch name, acts as a prefix, followed by a slash.

**PBI**  
Optionally, when using Agile project management, the Product Backlog Item (PBI) number goes here.

**User**  
Three letters representing the username. For example, denczh -> dnc.

**Description**  
Each branch is created with a purpose, encoded as a single, simple kebab-case phrase. The phrase should be as short as possible, no more than 60-70 characters, starting with a nominal phrase. Use abbreviations and avoid articles.

The full branch name will thus be:

```
name/user-PBI(optional)-description
```

Example:

```
ftr/dnc-1234-addition-of-toolbar-to-character-creation-section
```

## CI/CD
**PR from `ftr` or `fix` to `dev`**  
After PR approval (the branch must include documentation, unit tests, and integration tests), the CI sequence is triggered: build, test execution, and style verification (linting).

**PR from `dev` to `main`**  
The CI and CD sequences are triggered, publishing crates and creating the appropriate artifacts.