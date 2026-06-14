# Architecture

## Goal

Build a narrow developer workflow assistant that turns one small issue into selected files, a plan, a code result, test output, and a reviewer summary.

## System boundary

The first version should not attempt a general coding IDE. It should handle small, well-scoped issues and make every step easy to review.

## Components

| Component | Responsibility |
|---|---|
| Web UI | Issue intake, repo map, selected files, plan, result, test output, review summary |
| GitHub adapter | Read issue data and repository files |
| Repo mapper | Summarize folders, package manager, and test command |
| File selector | Choose relevant files with reasons |
| Planner | Write a small plan before code changes |
| Code runner | Run tests or mock test commands |
| Summary writer | Generate reviewer-friendly notes |
| Record store | Store task, selected files, plan, result, and test output |

## MVP flow

```text
Read issue
  -> parse accepted criteria
  -> build repo map
  -> select files
  -> write plan
  -> produce result
  -> run tests
  -> write review summary
```

## Recommended first stack

- Frontend: React / Next.js / Tailwind
- Backend: FastAPI or Spring Boot
- GitHub API: issue and file read first
- Sandbox: local command allowlist later
- Database: SQLite or PostgreSQL

## Design principle

The project should make review easier. It should keep scope narrow and make file selection explainable.
