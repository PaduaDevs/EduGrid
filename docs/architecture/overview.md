# EduGrid Architecture Overview

## Context

EduGrid is an academic timetable optimization platform. The system must manage institutional data and generate timetables that satisfy mandatory constraints while optimizing preferences.

## Component view

```text
User
  |
  v
Web (Next.js)
  |
  | REST / OpenAPI
  v
API (NestJS)
  | \
  |  \ HTTP
  |   v
  |  Solver (FastAPI + OR-Tools CP-SAT)
  |
  v
PostgreSQL
```

## Responsibilities

### Web

- user interface;
- forms and validation feedback;
- timetable visualization;
- conflict presentation;
- interaction with the API.

The web application does not access PostgreSQL or the solver directly.

### API

- authentication/authorization when introduced;
- domain rules;
- CRUD operations;
- validation;
- persistence orchestration;
- solver requests;
- OpenAPI contract;
- audit/history coordination.

### Database

- relational domain state;
- referential integrity;
- migrations;
- scheduling inputs;
- schedule/run history.

### Solver

- translate scheduling inputs into a CP-SAT model;
- enforce hard constraints;
- score soft constraints;
- return assignments and optimization metadata.

The solver is not responsible for product CRUD or direct user interaction.

## Initial integration flow

```text
Web
 -> API
 -> load/validate scheduling data
 -> Solver
 -> optimization result
 -> API persists ScheduleRun + ScheduleAssignments
 -> Web receives result
```

## Architectural principle

Optimization is treated as a dedicated bounded technical concern rather than a collection of conditional statements embedded in CRUD services.
