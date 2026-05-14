# Usaha Hub API

Usaha Hub API adalah project belajar Spring Boot berbasis studi kasus UMKM Management System.

Tujuan utama repo ini bukan hanya membuat backend, tetapi juga membangun kebiasaan engineering yang rapi:

- build feature kecil
- pahami konsep Spring Boot
- dokumentasikan seperlunya
- update progress sprint
- commit perubahan secara bertahap

## Project Management

Project ini tidak memakai Jira di fase awal.

Semua context project dikelola langsung di repository:

- `docs/00-project` - visi produk, scope, glossary, tech stack
- `docs/01-roadmap` - roadmap belajar dan backend
- `docs/02-sprints` - sprint notes dan checklist task
- `docs/03-architecture` - catatan architecture
- `docs/04-learning-notes` - catatan belajar Spring Boot
- `docs/05-decisions` - Architecture Decision Records
- `docs/06-api` - dokumentasi API per module
- `docs/07-review` - review, refactor plan, mistakes log

## Current Focus

Current topic:

- setup repository learning management
- setup Spring Boot project
- prepare Sprint 00

Lihat sprint aktif di:

`docs/02-sprints/sprint-00-setup.md`

## Planned Tech Stack

- Java 21
- Spring Boot 3.4.x
- Maven
- PostgreSQL 16
- Docker Desktop on Windows
- Postman
- IntelliJ IDEA
- Git Bash or PowerShell

## Learning Workflow

Setiap topik Spring Boot mengikuti alur:

1. Learn concept
2. Implement feature
3. Commit code
4. Write short learning note
5. Update sprint checklist

## Commit Style

Gunakan format commit yang singkat dan jelas:

```text
feat(product): add create product endpoint
docs(sprint): update sprint 00 checklist
test(product): add product service test
refactor(product): simplify product mapper
```

