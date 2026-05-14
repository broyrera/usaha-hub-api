# System Overview

## Context

Usaha Hub API is a backend service for UMKM management.

In the learning phase, the system starts as a monolith Spring Boot application.

## High Level Flow

```text
Client
  -> REST API Controller
  -> Service
  -> Repository
  -> PostgreSQL
```

## Initial Modules

- Product
- Auth
- Sales
- Common

## Architecture Rule

Keep the first version simple. Use layered architecture before introducing more advanced patterns.

