```markdown
# qmd Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches best practices and conventions for contributing to the `qmd` TypeScript codebase. You'll learn about file naming, import/export styles, commit conventions, and the main workflow for bugfixes, including how to write and update tests and changelogs. This guide ensures consistency and quality across the project.

## Coding Conventions

- **Language:** TypeScript
- **Framework:** None detected
- **File Naming:** Use camelCase for all file names.
  - Example: `store.ts`, `pathFidelity.test.ts`
- **Import Style:** Use relative imports.
  - Example:
    ```typescript
    import { getStore } from './store'
    ```
- **Export Style:** Use named exports.
  - Example:
    ```typescript
    export function getStore() { ... }
    ```
- **Commit Messages:** Follow [Conventional Commits](https://www.conventionalcommits.org/) with prefixes like `fix` and `test`.
  - Example: `fix(store): correct path resolution logic`

## Workflows

### Bugfix with Tests and Changelog
**Trigger:** When you need to fix a bug and ensure it is tested and documented.  
**Command:** `/bugfix-with-tests`

1. **Identify and Fix the Bug**
   - Locate the bug in implementation files such as:
     - `src/store.ts`
     - `src/mcp/server.ts`
     - `src/cli/qmd.ts`
   - Apply the necessary code changes.
   - Example:
     ```typescript
     // src/store.ts
     export function getStore() {
       // fixed logic here
     }
     ```

2. **Update or Add Relevant Tests**
   - Modify or create test files in the `test/` directory:
     - `test/mcp.test.ts`
     - `test/store.test.ts`
     - `test/path-fidelity.test.ts`
   - Use [vitest](https://vitest.dev/) for testing.
   - Example:
     ```typescript
     // test/store.test.ts
     import { getStore } from '../src/store'

     test('getStore returns expected result', () => {
       expect(getStore()).toBe(/* expected value */)
     })
     ```

3. **Document the Change**
   - Add an entry to `CHANGELOG.md` describing the bugfix.
   - Example:
     ```
     ## [Unreleased]
     - fix(store): correct path resolution logic
     ```

4. **Commit Your Changes**
   - Use a conventional commit message, e.g.:
     ```
     fix(store): correct path resolution logic
     ```

## Testing Patterns

- **Testing Framework:** [vitest](https://vitest.dev/)
- **Test File Pattern:** All test files are named with the `.test.ts` suffix and placed in the `test/` directory.
  - Example: `test/store.test.ts`
- **Test Example:**
  ```typescript
  import { someFunction } from '../src/someModule'

  test('someFunction behaves correctly', () => {
    expect(someFunction()).toBe(true)
  })
  ```

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /bugfix-with-tests   | Start a bugfix workflow: fix code, update/add tests, changelog |
```
