# Product API

## Base Path

```text
/api/v1/products
```

## Planned Endpoints

### Create Product

```text
POST /api/v1/products
```

Request draft:

```json
{
  "name": "Kopi Susu",
  "description": "Minuman kopi susu botol",
  "sku": "KOPI-SUSU-001",
  "sellingPrice": 15000,
  "costPrice": 9000,
  "stock": 20,
  "minimumStock": 5,
  "active": true
}
```

Response draft:

```json
{
  "message": "Success",
  "data": {
    "id": 1,
    "name": "Kopi Susu",
    "description": "Minuman kopi susu botol",
    "sku": "KOPI-SUSU-001",
    "sellingPrice": 15000,
    "costPrice": 9000,
    "stock": 20,
    "minimumStock": 5,
    "active": true
  }
}
```

### List Products

```text
GET /api/v1/products
```

Response draft:

```json
{
  "message": "Success",
  "data": [
    {
      "id": 1,
      "name": "Kopi Susu",
      "description": "Minuman kopi susu botol",
      "sku": "KOPI-SUSU-001",
      "sellingPrice": 15000,
      "costPrice": 9000,
      "stock": 20,
      "minimumStock": 5,
      "active": true
    }
  ]
}
```

## Validation Rules

- `name` is required.
- `sellingPrice` is required and must be greater than or equal to 0.
- `costPrice` is optional and must be greater than or equal to 0 when provided.
- `stock` defaults to 0 and must be greater than or equal to 0.
- `minimumStock` defaults to 0 and must be greater than or equal to 0.
- `active` defaults to true.

## Notes

Product API follows wrapped response convention from `docs/03-architecture/api-conventions.md`.

