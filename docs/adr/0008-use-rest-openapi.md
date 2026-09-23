# ADR-0008 — Use REST and OpenAPI

## Status

Accepted

## Context

The web application needs a clear, inspectable, and documentable contract with the backend.

## Decision

Use REST endpoints documented through OpenAPI for the application API.

## Alternatives considered

- GraphQL
- tRPC
- ad-hoc undocumented HTTP endpoints

## Consequences

- language-agnostic contract;
- Swagger/OpenAPI documentation;
- straightforward testing and portfolio demonstration;
- contract changes must be reviewed for compatibility.
