# Sprint 01 - REST API Foundation

## Sprint Goal

Build basic Product CRUD API using Spring MVC.

## Learning Focus

- Spring MVC
- Controller
- DTO
- Service Layer
- Validation
- Global Exception Handling

## Stories

### Story 1 - OWNER can create product

#### Why

UMKM needs to register products before selling them.

#### Tasks

- [ ] Create Product entity or temporary model
- [ ] Create CreateProductRequest DTO
- [ ] Create ProductResponse DTO
- [ ] Create ProductService
- [ ] Create ProductController
- [ ] Add validation
- [ ] Test endpoint using Postman

#### Acceptance Criteria

- [ ] Product can be created using `POST /api/v1/products`
- [ ] Invalid request returns validation error
- [ ] Response uses DTO, not entity
- [ ] Code uses service layer

### Story 2 - OWNER can view product list

#### Tasks

- [ ] Add list products endpoint
- [ ] Return product response DTO list
- [ ] Test endpoint using Postman

#### Acceptance Criteria

- [ ] Product list can be fetched using `GET /api/v1/products`
- [ ] Response does not expose entity directly
