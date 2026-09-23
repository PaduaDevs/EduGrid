# ADR-0001 — Use TypeScript for Web and API

## Status

Accepted

## Context

The web and business API benefit from shared language knowledge, static typing, mature tooling, and a large ecosystem.

## Decision

Use TypeScript for the Next.js web application and NestJS API.

## Alternatives considered

- JavaScript without static typing
- Java
- C#
- Python for the entire application

## Consequences

- shared TypeScript knowledge across web/API;
- strong editor and refactoring support;
- type errors caught before runtime;
- the optimization engine remains free to use Python where its ecosystem is stronger.
