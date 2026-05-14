# System Overview

## Context

Usaha Hub API is a backend service for UMKM management.

In the learning phase, the system starts as a layered modular monolith Spring Boot application.

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

## Product Boundary

The system helps UMKM manage products, simple stock, sales transactions, and basic reports.

It does not cover full ERP, accounting, marketplace, multi-tenant SaaS, or payment gateway features in the early phase.

## Architecture Rule

Keep the first version simple. Use layered architecture before introducing more advanced patterns.
