# Database Design

## Database

PostgreSQL 16.

## Initial Tables

Planned early tables:

- `products`
- `users`
- `sales`
- `sale_items`

## Naming Convention

Tables use snake_case plural names:

- `products`
- `users`
- `sales`
- `sale_items`

Columns use snake_case:

- `created_at`
- `updated_at`
- `selling_price`
- `cost_price`
- `minimum_stock`

Java fields use camelCase:

- `createdAt`
- `updatedAt`
- `sellingPrice`
- `costPrice`
- `minimumStock`

## Product Table Draft

```text
products
- id
- name
- description
- sku
- selling_price
- cost_price
- stock
- minimum_stock
- active
- created_at
- updated_at
```

Rules:

- `name` is required.
- `sku` is optional in the early phase.
- `selling_price` is required and must be greater than or equal to 0.
- `cost_price` is optional in the early phase.
- `stock` defaults to 0 and must be greater than or equal to 0.
- `minimum_stock` defaults to 0 and must be greater than or equal to 0.
- `active` defaults to true.

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

Rules:

- `email` must be unique.
- `password_hash` must never be returned by API.
- Initial roles are `OWNER` and `STAFF`.

## Sales Table Draft

```text
sales
- id
- invoice_number
- payment_method
- status
- total_amount
- created_at
- updated_at
```

Rules:

- Initial payment methods are `CASH`, `QRIS`, and `TRANSFER`.
- Initial statuses are `COMPLETED` and `CANCELLED`.
- Cancel sale is not implemented in the first sales sprint.

## Sale Items Table Draft

```text
sale_items
- id
- sale_id
- product_id
- product_name
- quantity
- unit_price
- subtotal
- created_at
- updated_at
```

Rules:

- `quantity` must be greater than 0.
- `unit_price` stores the selling price at transaction time.
- `subtotal` is calculated from `quantity * unit_price`.

## Notes

Database design can evolve after API behavior is clearer.

