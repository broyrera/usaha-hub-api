# Package Structure

## Base Package

```text
com.usahahub.api
```

## Initial Structure

```text
com.usahahub.api
+-- product
|   +-- controller
|   +-- dto
|   +-- entity
|   +-- repository
|   `-- service
+-- auth
|   +-- controller
|   +-- dto
|   +-- entity
|   +-- repository
|   `-- service
+-- sales
+-- common
`-- config
```

## Rule

- Controller handles HTTP.
- Controller must not contain business logic.
- Service handles business logic.
- Repository handles database access.
- DTO handles API input and output.
- Entity should not be returned directly from controller.
- Manual DTO mapping is allowed in the early phase.
- Lombok and MapStruct are not used in the early phase.

