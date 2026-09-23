# ADR-0005 — Use Python and OR-Tools for the scheduling solver

## Status

Accepted

## Context

School timetabling is a combinatorial constraint optimization problem rather than a conventional CRUD rule set.

## Decision

Use Python and Google OR-Tools CP-SAT for the optimization engine, exposed through a small FastAPI service.

## Alternatives considered

- custom greedy algorithms only;
- embedding scheduling rules directly in NestJS;
- Timefold/Spring Boot;
- using an LLM to generate schedules.

## Consequences

- hard and soft constraints can be modelled explicitly;
- optimization behavior can be tested with datasets;
- the project introduces a second runtime ecosystem;
- API/solver contracts must be versioned and tested.
