# Sprint 0 — Foundation & Architecture

## Goal

Establish EduGrid's technical, organizational, and architectural foundation before feature development begins.

At the end of Sprint 0, a contributor should be able to clone the repository, start the main services, understand the domain and architecture, make a scoped change, run tests, and open a Pull Request with CI validation.

## Baseline stack

- Web: Next.js + React + TypeScript
- API: NestJS + TypeScript
- Database: PostgreSQL
- ORM: Prisma
- Solver: Python + FastAPI + Google OR-Tools CP-SAT
- Workspace: pnpm + Turborepo
- Local infrastructure: Docker Compose
- CI: GitHub Actions
- API contract: REST + OpenAPI

## Planned repository structure

```text
EduGrid/
├── apps/
│   ├── web/
│   └── api/
├── services/
│   └── solver/
├── packages/
│   ├── contracts/
│   ├── eslint-config/
│   └── typescript-config/
├── database/
│   ├── migrations/
│   └── seeds/
├── docs/
│   ├── architecture/
│   ├── adr/
│   ├── constraints/
│   ├── database/
│   ├── domain/
│   └── testing/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── workflows/
│   └── pull_request_template.md
├── docker-compose.yml
├── pnpm-workspace.yaml
├── turbo.json
├── CONTRIBUTING.md
└── README.md
```

## Sprint backlog

| ID | Task | Area | Priority |
|---|---|---|---|
| S0-01 | Bootstrap monorepo workspace | Infra | P0 |
| S0-02 | Bootstrap Next.js web application | Web | P0 |
| S0-03 | Bootstrap NestJS API | API | P0 |
| S0-04 | Configure PostgreSQL development environment | Database | P0 |
| S0-05 | Configure Prisma and initial migrations | Database/API | P0 |
| S0-06 | Design initial ERD | Database | P0 |
| S0-07 | Define domain glossary | Docs | P0 |
| S0-08 | Define scheduling constraint catalog | Solver | P0 |
| S0-09 | Bootstrap Python solver service | Solver | P0 |
| S0-10 | Implement OR-Tools solver spike | Solver | P0 |
| S0-11 | Configure Docker Compose | Infra | P1 |
| S0-12 | Configure web CI | Web/Infra | P1 |
| S0-13 | Configure API CI | API/Infra | P1 |
| S0-14 | Configure solver CI | Solver/Infra | P1 |
| S0-15 | Improve project README | Docs | P1 |
| S0-16 | Create CONTRIBUTING guide | Docs | P1 |
| S0-17 | Document initial ADRs | Docs | P1 |
| S0-18 | Configure Pull Request template | Infra | P2 |
| S0-19 | Configure Issue templates | Infra | P2 |
| S0-20 | Create demo scheduling dataset | Database | P1 |
| S0-21 | Implement integrated smoke test | Infra | P0 |

## Recommended execution order

```text
S0-01 Monorepo
├── S0-02 Web
├── S0-03 API
└── S0-09 Solver

S0-04 PostgreSQL
└── S0-05 Prisma
    └── S0-06 ERD

S0-07 Domain glossary
└── S0-08 Constraint catalog
    └── S0-10 Solver spike
```

After those foundations, continue with Docker, CI, documentation hardening, datasets, and the integrated smoke test.

## Sprint 0 success criteria

- repository structure is established;
- web, API, database, and solver can be started locally;
- `/api/health` or equivalent responds successfully;
- initial database migration is reproducible;
- ERD v0 is documented;
- domain glossary exists;
- hard and soft constraints are catalogued;
- solver produces a valid result for a small feasible dataset;
- solver returns infeasible for an intentionally impossible dataset;
- CI is green;
- another developer can follow the README and run the project.
