# Engineering Rules

## Architecture

- Use layered modular monolith architecture first.
- Controller handles HTTP only.
- Controller must not contain business logic.
- Service handles business logic.
- Repository handles database access.
- DTO handles API input and output.
- Entity must not be returned directly from controller.
- Exception response must be standardized after global exception handler is added.

## Code Style

- Use constructor injection.
- Prefer clear naming over clever abstraction.
- Avoid unrelated refactor.
- Keep implementation small and focused.
- Use manual DTO mapping first.
- Do not use MapStruct in the early phase.
- Do not use Lombok in the early phase.

## Learning Rule

Every feature should teach one or more backend concepts.

Examples:

- Health endpoint teaches Spring Boot startup and controller basics.
- Product create teaches Spring MVC, DTO, and validation.
- Product persistence teaches Spring Data JPA and repository.
- Register and login teach Spring Security and password hashing.
- Sales transaction teaches transaction boundary and business rules.
- Report teaches query and aggregation.

## Documentation Rule

- Document only when it helps learning or future maintenance.
- Update sprint checklist after finishing a task.
- Put mistakes in `docs/07-review/mistakes-log.md`.
- Put cleanup ideas in `docs/07-review/refactor-plan.md`.

## Git Rule

- Sprint 00 and Sprint 01 can use `main` only.
- Start using `feature/*` branches from Sprint 02 if the workflow still feels manageable.
- Keep commits small and descriptive.

