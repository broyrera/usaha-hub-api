# Sprint 03 - Authentication

## Sprint Goal

Add basic authentication using Spring Security and JWT.

## Learning Focus

- Spring Security
- password hashing
- authentication flow
- JWT
- protected endpoints

## Stories

### Story 1 - User can register account

#### Tasks

- [ ] Create User entity
- [ ] Create register request DTO
- [ ] Hash password
- [ ] Save user to database
- [ ] Return safe response DTO

#### Acceptance Criteria

- [ ] Password is never returned in API response
- [ ] Password is stored as hash
- [ ] Duplicate email is rejected

### Story 2 - User can login

#### Tasks

- [ ] Create login request DTO
- [ ] Validate credentials
- [ ] Generate JWT
- [ ] Return token response

#### Acceptance Criteria

- [ ] Valid credentials return JWT
- [ ] Invalid credentials return proper error
- [ ] Protected endpoints require token

