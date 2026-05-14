# ADR 001 - Use Layered Architecture

## Status

Accepted

## Context

This project is a Spring Boot learning project. The first architecture should be easy to understand and close to common backend practices.

## Decision

Use layered architecture:

```text
Controller -> Service -> Repository
```

## Consequences

Positive:

- beginner-friendly
- easy to test concept by concept
- matches common Spring Boot tutorials and production code

Tradeoff:

- can become repetitive as modules grow
- may need refactor if business logic becomes more complex

