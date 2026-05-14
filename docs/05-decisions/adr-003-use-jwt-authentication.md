# ADR 003 - Use JWT Authentication

## Status

Proposed

## Context

The project will need authentication for admin and protected endpoints.

## Decision

Use JWT authentication after Spring Security basics are understood.

## Consequences

Positive:

- common backend API authentication pattern
- good learning path for stateless security

Tradeoff:

- security implementation needs care
- token expiration and refresh strategy must be designed later

