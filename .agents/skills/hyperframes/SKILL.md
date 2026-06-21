```markdown
# hyperframes Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `hyperframes` TypeScript codebase. You'll learn how to structure files, write code, and follow commit and testing conventions to ensure consistency and maintainability. This guide is ideal for contributors or teams adopting similar patterns in TypeScript projects without a framework.

## Coding Conventions

### File Naming
- **Style:** kebab-case
- **Example:**  
  ```
  hyper-frames.ts
  data-processor.test.ts
  ```

### Import Style
- **Style:** Relative imports
- **Example:**
  ```typescript
  import { processData } from './data-processor';
  ```

### Export Style
- **Style:** Named exports
- **Example:**
  ```typescript
  // In data-processor.ts
  export function processData(input: string): string { ... }
  ```

### Commit Messages
- **Type:** Conventional commits
- **Prefix:** `feat`
- **Average Length:** ~58 characters
- **Example:**
  ```
  feat: add support for processing multiple data frames
  ```

## Workflows

### Adding a New Feature
**Trigger:** When you want to introduce a new feature.
**Command:** `/add-feature`

1. Create a new TypeScript file using kebab-case (e.g., `new-feature.ts`).
2. Implement your feature using named exports.
3. Import dependencies using relative paths.
4. Write corresponding test(s) in a file named `new-feature.test.ts`.
5. Commit your changes using the conventional commit format:
   ```
   feat: brief description of the new feature
   ```
6. Open a pull request for review.

### Writing Tests
**Trigger:** When you add or update code that requires testing.
**Command:** `/write-test`

1. Create a test file matching the pattern `*.test.ts` (e.g., `data-processor.test.ts`).
2. Write your tests using your preferred testing framework (framework not specified).
3. Use relative imports to bring in the module(s) under test.
4. Run your tests using the project's test runner.

## Testing Patterns

- **Test File Naming:**  
  Test files follow the `*.test.ts` pattern and are placed alongside the files they test.
  - Example:  
    ```
    data-processor.ts
    data-processor.test.ts
    ```
- **Framework:**  
  Not specified; use your preferred TypeScript-compatible test runner.
- **Import Style:**  
  Use relative imports in test files.
  - Example:
    ```typescript
    import { processData } from './data-processor';
    ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-feature   | Start the workflow for adding a new feature  |
| /write-test    | Begin writing tests for a module or feature  |
```
