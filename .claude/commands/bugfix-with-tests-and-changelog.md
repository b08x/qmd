---
name: bugfix-with-tests-and-changelog
description: Workflow command scaffold for bugfix-with-tests-and-changelog in qmd.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bugfix-with-tests-and-changelog

Use this workflow when working on **bugfix-with-tests-and-changelog** in `qmd`.

## Goal

Implements a bugfix that updates implementation code, adds or updates corresponding tests, and documents the change in the changelog.

## Common Files

- `src/store.ts`
- `src/mcp/server.ts`
- `src/cli/qmd.ts`
- `test/mcp.test.ts`
- `test/store.test.ts`
- `test/path-fidelity.test.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify and fix the bug in implementation files (e.g., src/store.ts, src/mcp/server.ts, src/cli/qmd.ts).
- Update or add relevant test files (e.g., test/mcp.test.ts, test/store.test.ts, test/path-fidelity.test.ts).
- Document the change in CHANGELOG.md.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.