# Issue-to-PR Coding Agent

A focused developer-workflow agent that turns one small GitHub issue into a clear review package: accepted criteria, selected files, change plan, code result, test output, and reviewer summary.

This project does not try to build a full IDE. It focuses on one narrow workflow: understand the issue, select context, plan a small change, run tests, and produce a result a human can review quickly.

## Why this project exists

AI coding tools can generate code quickly. The harder problem is making changes that are small, relevant, tested, and easy to review.

A useful coding agent should answer:

1. What is the issue asking for?
2. What are the accepted criteria?
3. Which files are relevant, and why?
4. What is the smallest reasonable change?
5. What tests were run?
6. What should the reviewer check?

## Product shape

The product should feel like a compact review assistant for small issues.

Core screens:

| Screen | What it shows |
|---|---|
| Issue Intake | Title, body, labels, accepted criteria |
| Repository Map | Project structure, package manager, test command |
| Selected Files | Files chosen for the change, with short reasons |
| Change Plan | Small plan before implementation |
| Code Result | What changed and where |
| Test Output | Command, result, and short notes |
| Review Summary | What the reviewer should inspect |

## MVP target

Build a narrow coding agent that reads a small GitHub issue, selects relevant files, writes a change plan, produces a small result, runs tests, and writes a review summary.

```text
issue -> criteria -> repo map -> selected files -> plan -> result -> tests -> review summary
```

The first demo should show that the system makes code review easier instead of hiding the work.

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Supported issue types and demo repo | The agent has a narrow and believable scope |
| P0 / MVP | Issue intake and repo map | The agent understands the task before editing |
| P0 / MVP | Relevant file retrieval | The agent avoids loading the whole repository blindly |
| P0 / MVP | Showcase path | One demo path from issue intake to review summary |
| P1 | Plan and minimal code result | The change is reviewable before tests run |
| P1 | Test runner and one repair note | Test feedback becomes part of the loop |
| P1 | Draft PR summary | Human reviewers can inspect the result quickly |
| P2 | Interview notes and demo script | The project is easy to explain to AI devtools teams |

## Repository documents

- [Roadmap](docs/roadmap.md)
- [Business Context](docs/business-context.md)
- [Demo Notes](docs/demo-notes.md)
- [Design Gallery](docs/design-gallery.md)

## Demo narrative

1. Select a small GitHub issue.
2. Show the accepted criteria.
3. Show the repository map and selected files.
4. Generate a small change plan.
5. Show the result.
6. Show test output.
7. Show a reviewer-friendly summary.

## What this project demonstrates

- Context engineering for coding tasks.
- Narrow scope control and file selection discipline.
- Test-aware development loop.
- Clear communication for human reviewers.
- Strong fit for AI devtools and developer productivity roles.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap. The next build target is the P0 MVP showcase path.
