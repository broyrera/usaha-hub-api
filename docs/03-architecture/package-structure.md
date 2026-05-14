# Package Structure

## Base Package

```text
com.usahahub.api
```

## Initial Structure

```text
com.usahahub.api
├── product
│   ├── controller
│   ├── dto
│   ├── entity
│   ├── repository
│   └── service
├── auth
│   ├── controller
│   ├── dto
│   ├── entity
│   ├── repository
│   └── service
├── sales
├── common
└── config
```

## Rule

- Controller handles HTTP.
- Service handles business logic.
- Repository handles database access.
- DTO handles API input and output.
- Entity should not be returned directly from controller.

