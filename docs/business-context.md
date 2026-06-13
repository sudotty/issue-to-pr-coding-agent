# Business Context

## Who this is for

This project is for engineering teams that want AI coding help without losing code review discipline.

Typical users:

- Developer productivity teams.
- AI devtools teams.
- Small engineering teams with many small issues.
- Maintainers who want draft changes, not blind automation.

## Business problem

AI can produce code quickly. The harder question is whether the change is small, relevant, tested, and easy to review.

Common failure points:

1. The agent loads too much context.
2. It edits too many files.
3. It cannot explain why files were selected.
4. It produces a patch without tests.
5. The reviewer cannot understand the change quickly.

## Product wedge

This project focuses on the narrow path from issue to draft PR:

- parse issue and acceptance criteria
- build a repository map
- retrieve relevant files
- write a change plan
- generate a minimal patch
- run tests
- create a reviewer-friendly summary

The practical message is simple: a coding agent should make review easier, not hide complexity.

## Demo story

A user selects a small GitHub issue. The system reads the issue, finds relevant files, proposes a plan, creates a minimal patch, runs tests, and writes a draft PR summary.

## Hiring signal

This project demonstrates context engineering, developer workflow understanding, and the judgment to keep AI coding narrow and reviewable.
