# ADR-0003 — Use NestJS for the backend API

## Status

Accepted

## Context

The API needs modular organization, dependency injection, testing support, validation, and OpenAPI integration.

## Decision

Use NestJS with TypeScript for the primary business API.

## Alternatives considered

- Express
- Fastify without a higher-level framework
- Spring Boot
- FastAPI as the sole backend

## Consequences

- explicit modules/controllers/providers;
- consistent dependency injection and testing patterns;
- OpenAPI integration;
- solver concerns remain isolated in the Python service.
