```markdown
# onetcli Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `onetcli` TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit message conventions, and understand the project's testing approach. This guide is ideal for contributors seeking to maintain consistency and quality in the codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** for functions, classes, or constants.
  - Example:
    ```typescript
    // dataFetcher.ts
    export function fetchData() { ... }
    ```

### Commit Messages
- Commit messages are generally **freeform**.
- Some commits may use the `[ImgBot]` prefix for image optimization.
- Average commit message length: ~24 characters.

  Example:
  ```
  [ImgBot] Optimize images
  Add new CLI option
  ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new CLI feature or module  
**Command:** `/add-feature`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Use relative imports to include dependencies.
3. Export your feature using named exports.
4. Write a corresponding test file named `newFeature.test.ts`.
5. Commit changes with a clear, concise message.

### Optimizing Images
**Trigger:** When updating or optimizing image assets  
**Command:** `/optimize-images`

1. Use an image optimization tool or script.
2. Commit with the `[ImgBot]` prefix in the message.
   - Example: `[ImgBot] Optimize images`

### Writing Tests
**Trigger:** When adding or updating functionality  
**Command:** `/write-test`

1. Create a test file matching the pattern `*.test.ts` (e.g., `userProfile.test.ts`).
2. Write tests for all exported functions or modules.
3. Run your tests using the project's preferred testing tool.

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
- The specific testing framework is **unknown**, but standard TypeScript testing practices apply.
- Place test files alongside the modules they test or in a dedicated test directory.
- Example test file:
  ```typescript
  // userProfile.test.ts
  import { getUserProfile } from './userProfile';

  describe('getUserProfile', () => {
    it('should return user data', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command           | Purpose                                         |
|-------------------|-------------------------------------------------|
| /add-feature      | Scaffold and implement a new CLI feature/module |
| /optimize-images  | Optimize image assets and commit changes        |
| /write-test       | Create and run tests for new or updated code    |
```
