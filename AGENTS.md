# AI Context

This project is a Spring Boot learning project for building an UMKM management backend step by step.

## Goal

Build a beginner-friendly but production-style backend while learning Spring Boot concepts through implementation.

## Project Management Rule

Do not use Jira for this project phase.

Use repository-based project management:

- roadmap in `docs/01-roadmap`
- sprint checklist in `docs/02-sprints`
- architecture notes in `docs/03-architecture`
- learning notes in `docs/04-learning-notes`
- decisions in `docs/05-decisions`
- API docs in `docs/06-api`
- review notes and mistakes log in `docs/07-review`

## Technical Rules

- Use Java 21.
- Use Spring Boot 3.4.x.
- Use Maven.
- Use PostgreSQL.
- Use layered architecture first.
- Use DTOs for API request and response models.
- Do not expose JPA entities directly from controllers.
- Use constructor injection.
- Keep code beginner-friendly but production-style.
- Prefer clear naming over clever abstraction.
- Add documentation only when it helps learning or future maintenance.

## Backend Style

Preferred package direction:

```text
com.usahahub.api
├── product
├── auth
├── sales
├── common
└── config
```

Inside a module, prefer:

```text
controller
dto
entity
repository
service
```

## Workflow For AI Agents

When making changes:

1. Read the relevant sprint file first.
2. Read related architecture or API docs if they exist.
3. Implement the smallest useful step.
4. Update sprint checklist when a task is completed.
5. Add or update learning notes only when the concept is important.
6. Keep unrelated refactors out of the change.

## Current Project Phase

The project is in repository setup and Spring Boot foundation phase.

