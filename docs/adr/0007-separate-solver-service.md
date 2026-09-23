# ADR-0007 — Separate the optimization engine from the business API

## Status

Accepted

## Context

The API and solver have different responsibilities, runtimes, testing needs, and failure modes.

## Decision

Keep scheduling optimization in a dedicated Python service. NestJS remains the orchestration and business API boundary.

## Alternatives considered

- embed Python through subprocess calls;
- rewrite optimization in TypeScript;
- merge all backend responsibilities into FastAPI.

## Consequences

- clear ownership and boundaries;
- independent solver testing;
- an internal HTTP contract is required;
- distributed-service concerns must be kept minimal while the project is small.
