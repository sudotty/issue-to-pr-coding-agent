# Issue-to-PR Coding Agent

A focused coding agent that turns small GitHub issues into tested draft PRs with minimal, reviewable patches.

This project does not try to build a full IDE. It focuses on one engineering workflow: issue intake, repository context, change planning, patch generation, test feedback, repair, and PR summary.

## Why this project exists

AI coding tools can generate code quickly. The harder problem is making changes that are small, testable, reviewable, and safe.

A useful coding agent should answer:

1. What is the issue asking for?
2. Which files are relevant?
3. What is the smallest safe change?
4. Did the tests pass?
5. If tests failed, can the agent repair once?
6. Can a human reviewer understand the PR quickly?

## MVP target

Build a narrow coding agent that reads a small GitHub issue, selects relevant files, writes a change plan, proposes a minimal patch, runs tests, attempts one repair, and writes a draft PR summary.

```text
issue -> acceptance criteria -> repo map -> relevant files -> plan -> patch -> tests -> one repair -> draft PR summary
```

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Supported issue types and demo repo | The agent has a narrow and believable scope |
| P0 / MVP | Issue intake and repo map | The agent understands the task before editing |
| P0 / MVP | Relevant file retrieval | The agent avoids loading the whole repository blindly |
| P1 | Plan and minimal patch | The change is reviewable before tests run |
| P1 | Sandboxed tests and one repair | Test feedback becomes part of the loop |
| P1 | Draft PR summary | Human reviewers can inspect the result quickly |
| P2 | Interview notes and demo | The project is easy to explain to AI devtools teams |

## Core features

| Feature | Purpose |
|---|---|
| Issue intake | Read issue title, body, labels, acceptance criteria |
| Repo map | Summarize project structure and test layout |
| Relevant file retrieval | Avoid stuffing the whole repo into context |
| Change plan | Make the agent's intent reviewable |
| Patch generation | Produce minimal diffs |
| Test runner | Verify the change before PR |
| Repair loop | Use test output as feedback |
| PR summary | Explain files changed, tests run, and risks |
| Safety limits | Max files, command allowlist, no auto-merge |

## Interview value

This project helps explain repository context construction, narrow scope control, test feedback, repair loops, and why coding agents should produce reviewable draft PRs.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap.
