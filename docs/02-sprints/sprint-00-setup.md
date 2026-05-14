# Sprint 00 - Project Setup

## Sprint Goal

Prepare repository structure, documentation workflow, and Spring Boot project foundation.

## Learning Focus

- Git repository structure
- repo-based project management
- basic Spring Boot project setup
- Maven project structure

## Stories

### Story 1 - Repository has learning management structure

#### Why

Project context should live in the repository so progress is easy to track and AI agents can understand the project.

#### Tasks

- [x] Create `docs` folder structure
- [x] Create `README.md`
- [x] Create `AGENTS.md`
- [x] Create `CHANGELOG.md`
- [x] Create roadmap document
- [x] Create sprint 00 document
- [x] Review documentation structure

#### Acceptance Criteria

- [x] Repo contains `docs/00-project`
- [x] Repo contains `docs/01-roadmap`
- [x] Repo contains `docs/02-sprints`
- [x] Repo contains `docs/03-architecture`
- [x] Repo contains `docs/04-learning-notes`
- [x] Repo contains `docs/05-decisions`
- [x] Repo contains `docs/06-api`
- [x] Repo contains `docs/07-review`
- [x] Repo contains AI agent instructions

### Story 2 - Spring Boot project can run locally

#### Why

The learning project needs an executable backend foundation before feature work starts.

#### Tasks

- [ ] Generate Spring Boot project
- [ ] Add Java 21 configuration
- [ ] Add Maven dependencies
- [ ] Add `application.yml`
- [ ] Run application locally
- [ ] Add simple health endpoint or use actuator later

#### Acceptance Criteria

- [ ] Application starts without error
- [ ] Project uses Java 21
- [ ] Project uses Maven
- [ ] Basic package structure exists

### Story 3 - Definition layer is clear before coding

#### Why

Product, API, domain, and engineering rules should be explicit before generating the Spring Boot project.

#### Tasks

- [x] Define product identity
- [x] Define user roles
- [x] Define core domain terms
- [x] Define MVP boundary
- [x] Define learning rules
- [x] Define architecture rules
- [x] Define API response convention
- [x] Define product data model
- [x] Define sales business rules
- [x] Define authentication boundary
- [x] Define database naming convention
- [x] Define git workflow

#### Acceptance Criteria

- [x] `docs/00-project/domain-model.md` exists
- [x] `docs/03-architecture/api-conventions.md` exists
- [x] `docs/03-architecture/engineering-rules.md` exists
- [x] Glossary includes core domain terms
- [x] Product API draft uses the agreed product fields
- [x] Database draft follows naming convention

## Sprint Notes

Keep this sprint small. The goal is to prepare the workspace, not to build product features yet.
