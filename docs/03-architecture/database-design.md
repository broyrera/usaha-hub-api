# Database Design

## Database

PostgreSQL 16.

## Initial Tables

Planned early tables:

- `products`
- `users`
- `sales`
- `sale_items`

## Product Table Draft

```text
products
- id
- name
- description
- price
- stock
- created_at
- updated_at
```

## User Table Draft

```text
users
- id
- name
- email
- password_hash
- role
- created_at
- updated_at
```

## Notes

Database design can evolve after API behavior is clearer.

