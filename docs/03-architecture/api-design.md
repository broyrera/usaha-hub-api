# API Design

## Base Path

```text
/api/v1
```

## Response Rule

Controllers return DTOs, not entities.

## Error Rule

Use a consistent error response shape once global exception handling is added.

Draft:

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

## Planned Endpoints

Product:

- `POST /api/v1/products`
- `GET /api/v1/products`
- `GET /api/v1/products/{id}`
- `PUT /api/v1/products/{id}`
- `DELETE /api/v1/products/{id}`

Auth:

- `POST /api/v1/auth/register`
- `POST /api/v1/auth/login`

Sales:

- `POST /api/v1/sales`
- `GET /api/v1/sales`

