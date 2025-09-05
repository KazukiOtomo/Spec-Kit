# [PROJECT_NAME] Constitution

<!-- Example: Spec Constitution, TaskFlow Constitution, etc. -->

## Core Principles

### I. Test-Driven Development (TDD) Cycle (NON-NEGOTIABLE)

Strictly follow the Red → Green → Refactor cycle. Always write the simplest failing test first, implement the minimum code required to make the test pass, and refactor only after the tests are passing.

### II. Tidy First

Clearly separate structural changes (e.g., renaming, extracting methods, moving code) from behavioral changes (adding or modifying functionality). Never mix these two types of changes in the same commit. When necessary, always perform structural changes first.

### III. Strict Commit Discipline

Commit only when all tests are passing and all linter/compiler warnings have been resolved. Each commit must represent a single logical unit of work, and the commit message must clearly state whether it contains structural or behavioral changes. Use small, frequent commits.

### IV. Uncompromising Code Quality

Ruthlessly eliminate duplication and express intent clearly through naming and structure. Keep methods small and focused on a single responsibility. Always adopt the simplest solution that could possibly work (YAGNI).

### V. Incremental Implementation

Always follow the instructions in `plan.md`. Implement one test at a time, write just enough code to make it pass, and then improve the code's structure. Run all tests (except long-running ones) after every change.

## Development Workflow

The approach for any new feature must strictly follow these steps:

1.  Write a simple failing test for a small part of the feature.
2.  Implement the bare minimum of code to make the test pass.
3.  Run all tests to confirm they pass (Green).
4.  Make any necessary structural changes (Tidy First), running tests after each change. Commit structural changes separately.
5.  Add another test for the next small increment of functionality.
6.  Repeat the cycle until the feature is complete, keeping behavioral and structural changes in separate commits.

## Governance

This Constitution supersedes all other practices. All pull requests and reviews must verify compliance with these principles. Development must always proceed by addressing the next unmarked test found in `plan.md`.

**Version**: 1.0.0 | **Ratified**: 2025-09-06 | **Last Amended**: 2025-09-06
