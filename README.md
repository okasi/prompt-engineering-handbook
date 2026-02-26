# Prompt Engineering Handbook - Concise Prompts 📖

## Prompts to queue after significant additions/changes

### 1. 3x spam:
```md
Are you sure all work is complete? 
Be brutally honest. 
If any part is missing, unclear, or could be parallelized better 
— create more subagents right now and delegate.
```

### 2. 1x:
```md
When done, 
with fresh eyes, 
review your changes with 2 subagents, 
fix any issues, 
then repeat until no issues found.
```

---

## Prompts for refactoring

### 1. 
```md
Analyze the codebase and architecture to identify key components, data flow, and interfaces.
Update the AGENTS.md with a concise overview of essential modules,
interaction points, and initialization steps,
ensuring it is free from tech debt and reflects the current state,
as existing documentation may be outdated or misleading.
```

### 2. 
```md
Run npx knip --fix to automatically remove or refactor unused code and dependencies.
This helps clean up the codebase by eliminating unnecessary components.
```

### 3. 
```md
Run `npx npm-check-updates -u` to update package.json with the latest dependencies.
Then, run `npm install` to install the updated versions.
Check the changelogs for any breaking changes, make required adjustments, and ensure nothing is broken.
If issues arise, revert the version changes to the last working one and reinstall dependencies.
```

### 4. 
```md
Analyze the codebase and refactor it to improve readability, structure, and clarity
so that models like Codex or Claude Code can understand and modify it more effectively.
Focus on simplifying logic, clarifying naming, reducing complexity, and removing technical debt,
while preserving functionality and verifying correctness.
Update the AGENTS.md file to reflect any changes made to the codebase and ensure it remains clear, accurate and concise.
```

---

## Prompts for testing

### Whole app:
```md
Test the whole application thoroughly in a browser to automatically find and fix bugs and edge cases.
```

### Feature:
```md
Test the feature thoroughly in a browser to automatically find and fix bugs and edge cases.
```
