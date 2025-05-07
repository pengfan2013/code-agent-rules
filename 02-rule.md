## Instructions for Coding Agent

This file (docs/TASK\_LIST.md) is the central task management system for the project. The Coding Agent must follow these instructions to manage tasks effectively:

1.  **Read the Task Table**: Use the table below to identify tasks, sub-tasks, their status, dependencies, and completion dates.

2.  **Add New Tasks**: When a new task is assigned, add it to the table with:

    -   A clear task title and description.

    -   Sub-tasks (if any) as a comma-separated list.

    -   Status set to "Not Started".

    -   Dependencies (list other task titles that must be completed first; use "None" if none).

    -   Completion Date set to "N/A".

3.  **Follow Test-Driven Development (TDD)**:

    -   For each task, first write tests that define the expected behavior.

    -   Implement the code to make the tests pass.

    -   Refactor the code while ensuring tests continue to pass.

    -   No task should be marked as "Completed" until all associated tests are written and passing.

4.  **Update Task Status**:

    -   Set Status to "In Progress" when starting a task.

    -   Set Status to "Completed" only after verifying the task with passing tests.

    -   Update Completion Date to the current date (format: YYYY-MM-DD) when marking a task as Completed.

5.  **Check Dependencies**: Before starting a task, ensure all listed dependencies have a Status of "Completed". If dependencies are not met, prioritize those tasks first.

6.  **Commit Changes**: After updating the table, commit changes to the repository with a message like "Updated TASK\_LIST.md with task status".

7.  **Maintain Table Format**: Keep the table structure intact, ensuring columns align and entries are clear.

8.  **Autonomy**: Work through tasks without seeking user input unless the task list is complete or clarification is explicitly required.

## Test-Driven Development Workflow

For each task in the task list, follow this TDD workflow:

1. **Write Tests First**:
   - Create test files that define the expected behavior of the feature
   - Tests should initially fail since the implementation doesn't exist yet
   - Ensure tests cover all requirements and edge cases

2. **Implement the Feature**:
   - Write the minimum code necessary to make the tests pass
   - Focus on functionality first, then optimize
   - Ensure all tests pass after implementation

3. **Refactor**:
   - Improve code quality while maintaining test coverage
   - Eliminate code smells and technical debt
   - Ensure tests still pass after refactoring

4. **Document**:
   - Add comments and documentation as needed
   - Update relevant documentation files
   - Include examples of usage where appropriate

5. **Update Task Status**:
   - Mark the task as "In Progress" when writing tests
   - Only mark as "Completed" when all tests pass and code is refactored
   - Include test coverage metrics in task completion notes

This workflow ensures that all code is testable, requirements are clearly understood, and regressions are caught early.

## Task Table
| Task | Sub-Tasks | Status | Dependencies | Completion Date |
| ---- | --------- | ------ | ------------ | --------------- |