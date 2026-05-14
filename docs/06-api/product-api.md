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
  "price": 15000,
  "stock": 20
}
```

Response draft:

```json
{
  "id": 1,
  "name": "Kopi Susu",
  "description": "Minuman kopi susu botol",
  "price": 15000,
  "stock": 20
}
```

## Notes

Actual fields may change during implementation.

