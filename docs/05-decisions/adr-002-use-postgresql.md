# ADR 002 - Use PostgreSQL

## Status

Accepted

## Context

The project needs a relational database for product, user, sales, and reporting data.

## Decision

Use PostgreSQL 16 as the primary database.

## Consequences

Positive:

- common production database
- good fit for relational data
- useful skill for backend development

Tradeoff:

- needs local database setup
- Docker configuration may be needed for consistent development

