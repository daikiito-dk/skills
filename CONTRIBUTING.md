# Contributing

Thanks for helping improve the skills in this repository.

## Development loop

We prefer a small, evidence-based workflow:

```text
Issue → Branch → Implementation → Test → PR → Review → Fix → Merge
```

### 1. Open or find an Issue

Explain the problem, proposed improvement, and why it provides user value. Reuse an existing Issue when possible.

### 2. Create a focused branch

Use a descriptive branch name such as:

```text
feat/add-release-health-check
fix/skill-validation
chore/update-documentation
```

### 3. Implement the smallest useful change

Keep changes focused. Avoid adding complexity solely to increase GitHub activity.

### 4. Validate the change

For skill changes, check:

- Markdown renders correctly.
- The skill has a clear purpose and invocation.
- Instructions are internally consistent.
- Examples match the defined behavior.
- No secrets or private information are introduced.

### 5. Open a Pull Request

Describe:

- What changed
- Why it changed
- How it was validated
- Any known limitations

Link the relevant Issue.

### 6. Review and fix

Treat review feedback as part of development. Update the branch when changes are needed and re-run validation.

### 7. Merge

Merge when the change is understood, validated, and ready for the repository.

## Adding a new skill

A new skill should normally include:

- A clear problem it solves
- Explicit inputs and outputs
- Operational instructions
- Safety or limitation boundaries where relevant
- Examples or invocation guidance
- A validation approach

Prefer reusable, general rules over instructions tied to one temporary project.

## GitHub achievements

GitHub activity should be a consequence of real development. Do not create meaningless Issues, commits, PRs, reviews, discussions, or releases just to farm achievements.

A useful change that happens to create a contribution opportunity is good. An artificial contribution created only for an achievement is not.
