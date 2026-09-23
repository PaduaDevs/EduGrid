# Contributing to EduGrid

## Development workflow

1. Pick or create a GitHub Issue.
2. Create a branch from `main`.
3. Keep the change focused on the Issue scope.
4. Run the relevant quality gates locally.
5. Open a Pull Request.
6. Obtain at least one review and keep CI green before merge.

## Branch naming

- `feat/*`
- `fix/*`
- `docs/*`
- `refactor/*`
- `test/*`
- `chore/*`

Examples:

- `feat/teacher-domain`
- `feat/solver-spike`
- `docs/architecture`
- `chore/web-ci`

## Commits

EduGrid uses Conventional Commits.

Examples:

- `feat(api): add teacher module`
- `feat(web): create dashboard shell`
- `feat(solver): add teacher collision constraint`
- `docs(adr): document PostgreSQL decision`
- `test(solver): add infeasible schedule case`
- `ci(web): add frontend quality gate`

## Pull Requests

Every relevant change must go through a Pull Request.

A PR should include:

- problem/context;
- proposed solution;
- how to test;
- screenshots for UI changes;
- related Issue;
- relevant risks or limitations.

## Definition of Done

A task is considered done when, when applicable:

- implementation is complete;
- lint passes;
- typecheck passes;
- tests pass;
- build passes;
- documentation is updated;
- Pull Request is reviewed;
- CI is green;
- change is merged.

Architecture changes require an ADR.

Database changes require a migration and model documentation update.

Solver changes require a reproducible dataset or automated test.
