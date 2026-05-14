# API Conventions

## Base Path

```text
/api/v1
```

## Success Response

```json
{
  "message": "Success",
  "data": {}
}
```

## List Response

```json
{
  "message": "Success",
  "data": []
}
```

## Validation Error Response

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

## General Error Response

```json
{
  "message": "Product not found"
}
```

## Rules

- Controller returns DTO, not entity.
- Request body uses request DTO.
- Response body uses response DTO.
- Successful response uses wrapped response.
- Error response shape must be consistent.
- Use clear messages that are useful for API clients.

