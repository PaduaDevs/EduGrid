# ADR-0004 — Use PostgreSQL as the primary database

## Status

Accepted

## Context

EduGrid's domain is strongly relational: institutions, teachers, subjects, rooms, class groups, timeslots, curriculum requirements, schedules, and assignments are interconnected and require integrity guarantees.

## Decision

Use PostgreSQL as the primary database.

## Alternatives considered

- MySQL
- MongoDB
- Firebase/Firestore

## Consequences

- strong relational constraints and transactions;
- mature indexing/query capabilities;
- natural fit for normalized domain data;
- schema changes must be managed through migrations.
