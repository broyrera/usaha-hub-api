# AI Context

This project is a Spring Boot learning project for building an UMKM management backend step by step.

## Goal

Build a beginner-friendly but production-style backend while learning Spring Boot concepts through implementation.

Usaha Hub API is a modular monolith backend for helping UMKM manage products, simple stock, sales transactions, and basic reports.

It is not a full ERP, accounting system, marketplace, multi-tenant SaaS, or payment gateway app in the early phase.

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
- Use wrapped API responses.
- Use manual DTO mapping first.
- Do not use Lombok in the early phase.
- Do not use MapStruct in the early phase.
- Keep code beginner-friendly but production-style.
- Prefer clear naming over clever abstraction.
- Add documentation only when it helps learning or future maintenance.

## Product Rules

- Initial MVP includes Product CRUD, product persistence, basic auth, sales recording, and basic report.
- Product has `sellingPrice` and optional `costPrice`.
- Product stock cannot be negative.
- Sale reduces product stock.
- Sale cannot be created if product is inactive.
- Sale cannot be created if stock is insufficient.
- Initial user roles are `OWNER` and `STAFF`.
- Role-based authorization can be defined before it is implemented.

## Locked Decisions

- Project type is UMKM Management Backend.
- Architecture is layered modular monolith.
- API style is REST API.
- API response uses wrapped response.
- Initial module is Product.
- First executable goal is health endpoint.
- Early product storage may be in-memory before Sprint 02 database persistence.
- Docker is introduced later when database setup starts.

## API Rules

- Base path is `/api/v1`.
- Success response uses:

```json
{
  "message": "Success",
  "data": {}
}
```

- Validation error response uses:

```json
{
  "message": "Validation failed",
  "errors": [
    {
      "field": "name",
      "message": "must not be blank"
    }
  ]
}
```

## Database Naming

- Table names use snake_case plural names.
- Column names use snake_case.
- Java fields use camelCase.

## Backend Style

Preferred package direction:

```text
com.usahahub.api
+-- product
+-- auth
+-- sales
+-- common
`-- config
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
2. Read related domain, architecture, or API docs if they exist.
3. Implement the smallest useful step.
4. Update sprint checklist when a task is completed.
5. Add or update learning notes only when the concept is important.
6. Keep unrelated refactors out of the change.

## Current Project Phase

The project is in repository setup and Spring Boot foundation phase.
