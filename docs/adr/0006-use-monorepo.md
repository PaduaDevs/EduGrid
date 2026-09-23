# ADR-0006 — Use a monorepo

## Status

Accepted

## Context

EduGrid is developed by a small team and contains web, API, solver, shared contracts, database artifacts, and documentation that evolve together.

## Decision

Use a single repository organized as a monorepo with pnpm workspaces and Turborepo for Node/TypeScript workspaces.

## Alternatives considered

- separate repository per service;
- single unstructured repository.

## Consequences

- easier atomic changes across components;
- centralized documentation and CI;
- shared contracts/configuration can be versioned together;
- CI must avoid unnecessarily rebuilding unrelated components.
