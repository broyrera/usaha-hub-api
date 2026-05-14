# Auth API

## Base Path

```text
/api/v1/auth
```

## Authentication Boundary

Initial auth scope:

- register OWNER account
- login
- return JWT access token later
- protect product and sales endpoints later

Out of scope for the early phase:

- refresh token
- forgot password
- email verification
- OAuth Google
- multi-device session
- complex permission matrix

## Planned Endpoints

### Register

```text
POST /api/v1/auth/register
```

Request draft:

```json
{
  "name": "Budi",
  "email": "budi@example.com",
  "password": "password123"
}
```

Response draft:

```json
{
  "message": "Success",
  "data": {
    "id": 1,
    "name": "Budi",
    "email": "budi@example.com",
    "role": "OWNER"
  }
}
```

### Login

```text
POST /api/v1/auth/login
```

Request draft:

```json
{
  "email": "budi@example.com",
  "password": "password123"
}
```

Response draft:

```json
{
  "message": "Success",
  "data": {
    "accessToken": "jwt-token"
  }
}
```

## Password Rules

- Password must have at least 8 characters.
- Email must be unique.
- Password must be stored as hash.
- Password must never be returned in API response.

## Notes

Authentication will be implemented after REST API and database foundation are stable.

