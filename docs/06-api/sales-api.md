# Sales API

## Base Path

```text
/api/v1/sales
```

## Planned Endpoints

### Create Sale

```text
POST /api/v1/sales
```

Request draft:

```json
{
  "paymentMethod": "CASH",
  "items": [
    {
      "productId": 1,
      "quantity": 2
    }
  ]
}
```

Response draft:

```json
{
  "message": "Success",
  "data": {
    "id": 1,
    "invoiceNumber": "INV-20260514-001",
    "paymentMethod": "CASH",
    "status": "COMPLETED",
    "totalAmount": 30000,
    "items": [
      {
        "productId": 1,
        "productName": "Kopi Susu",
        "quantity": 2,
        "unitPrice": 15000,
        "subtotal": 30000
      }
    ]
  }
}
```

### List Sales

```text
GET /api/v1/sales
```

## Business Rules

- Sale contains one or more sale items.
- Sale item must reference a product.
- Total sale is calculated from subtotal of all items.
- Subtotal is calculated from `quantity * unitPrice`.
- Sale cannot be created if product is inactive.
- Sale cannot be created if stock is insufficient.
- Successful sale reduces product stock.
- Cancel sale is not implemented in the first sales sprint.

## Initial Values

Payment methods:

- `CASH`
- `QRIS`
- `TRANSFER`

Sale statuses:

- `COMPLETED`
- `CANCELLED`

## Notes

Sales API depends on Product and database persistence.

