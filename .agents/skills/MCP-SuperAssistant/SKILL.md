```markdown
# MCP-SuperAssistant Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development conventions and patterns used in the MCP-SuperAssistant repository, a TypeScript codebase built with React. It covers file organization, code style, commit practices, and testing patterns to ensure consistency and maintainability across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all filenames.
  - Example: `userProfile.tsx`, `dashboardHeader.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { UserProfile } from './userProfile';
    import { DashboardHeader } from '../components/dashboardHeader';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // userProfile.tsx
    export const UserProfile = () => { /* ... */ };
    ```

### Commit Messages
- Follow **Conventional Commits**.
- Use the `chore` prefix for general maintenance.
- Keep commit messages concise (average 75 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Creating a New Component
**Trigger:** When adding a new UI component to the project  
**Command:** `/create-component`

1. Create a new file using camelCase (e.g., `myNewComponent.tsx`).
2. Use a named export for the component.
3. Use relative imports for dependencies.
4. Add a corresponding test file named `myNewComponent.test.tsx`.

### Making a Commit
**Trigger:** When committing changes to the repository  
**Command:** `/commit-changes`

1. Stage your changes.
2. Write a commit message using the conventional format, e.g., `chore: describe your change`.
3. Keep the message under 75 characters.

### Adding a Test
**Trigger:** When adding or updating tests for a module  
**Command:** `/add-test`

1. Create a test file with the pattern `*.test.*` (e.g., `userProfile.test.tsx`).
2. Write tests for the corresponding module.
3. Use the project's preferred testing framework (unknown; check project docs).

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
- Each module/component should have a corresponding test file.
- The specific testing framework is not specified; refer to project documentation or existing tests for guidance.

## Commands
| Command             | Purpose                                      |
|---------------------|----------------------------------------------|
| /create-component   | Scaffold a new React component               |
| /commit-changes     | Make a commit following conventions          |
| /add-test           | Add or update a test for a module/component  |
```
