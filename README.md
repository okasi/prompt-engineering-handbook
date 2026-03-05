# Prompt Engineering Handbook - Concise Prompts 📖

## Spam queue:able prompts

### 2x review w/ subagents
```md
When done, with fresh eyes,
review your changes with 2 subagents,
fix any issues,
then repeat until no issues are found.

If anything is missing, unclear,
or could be parallelized better,
create more subagents right now and delegate.

Be brutally honest about whether all work is complete,
then repeat until no issues are found.
```

### Reverse engineering
```md
Continue reverse engineering.

1. Restate the MODEL + top UNKNOWNS.
2. Pick ONE highest-value next TARGET (why).
3. DEEP-DIVE: purpose, I/O + side effects, callers/callees, data/constants, ERROR paths.
4. If needed: STEP TRACE + PSEUDOCODE.
5. UPDATE: architecture, STATE MACHINE, ranked unknowns.
6. END: open questions, next target, PRESERVATION NOTE.

Continue until fully mapped and irreducible—stop only when zero meaningful unknowns remain.
```

### Implementation
```md
Continue implementation using the existing reverse-engineering docs as source of truth.

1. Restate the PLAN + top RISKS/BLOCKERS.
2. Pick ONE highest-value next CHANGE to ship (why).
3. IMPLEMENT: exact edits (where/what), configs/migrations, deps, and TESTS.
4. If needed: STEP-BY-STEP rollout + fallback/rollback.
5. UPDATE: architecture/state deltas, invariants, ranked remaining backlog.
6. END: what shipped, verification results, new issues, next change, PRESERVATION NOTE.

Continue until the work is COMPLETE and stable—stop only when zero critical TODOs remain.
```

---

## Refactoring prompts

### Update AGENTS.md
```md
Analyze the codebase and architecture to identify key components, data flow, and interfaces.
Update the AGENTS.md with a concise overview of essential modules,
interaction points, and initialization steps,
ensuring it is free from tech debt and reflects the current state,
as existing documentation may be outdated or misleading.
```

### JS/TS: Remove unused code & dependencies
```md
Run `npx knip --fix` to automatically remove or refactor unused code and dependencies.
This helps clean up the codebase by eliminating unnecessary components.
```

### JS/TS: Update dependencies
```md
Run `npx npm-check-updates -u` to update package.json with the latest dependencies.
Then, run `npm install` or `pnpm install` to install the updated versions.
Check the changelogs for any breaking changes, make required adjustments, and ensure nothing is broken.
If issues arise, revert the version changes to the last working one and reinstall dependencies.
```

### Complete overhaul
```md
Analyze the whole codebase and refactor it to improve readability, structure, and clarity,
ensuring that coding agents like Codex by OpenAI, Claude Code by Anthropic, and Copilot by GitHub can understand and modify it more effectively. 
Simplify logic, clarify naming, reduce complexity, eliminate technical debt,
and optimize performance to enhance efficiency, all while preserving functionality and verifying correctness. 
Ensure a minimal directory structure, align directory names with the material-icons naming convention. 
Update the AGENTS.md file to reflect any changes made to the codebase, ensuring it remains clear, accurate, and concise.
```

---

## Prompts for testing

### Whole app
```md
Test the whole application thoroughly using the appropriate tool (CLI or browser). 
For backend Node.js applications, write performant smoke tests using the built-in `node:test` module. 
For frontend applications, use `vitest` for smoke testing. 
Automatically identify and fix bugs and edge cases as you go.
```

### Specific feature
```md
Test the feature thoroughly using the appropriate tool (CLI or browser). 
For backend Node.js applications, write performant smoke tests using the built-in `node:test` module. 
For frontend applications, use `vitest` for smoke testing. 
Automatically identify and fix bugs and edge cases as you go.
```
