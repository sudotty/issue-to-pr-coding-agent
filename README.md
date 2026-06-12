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

## Core workflow

```text
GitHub issue
  ↓
Parse goal and acceptance criteria
  ↓
Build repo map
  ↓
Retrieve relevant files
  ↓
Generate change plan and risk notes
  ↓
Generate minimal patch
  ↓
Run tests in sandbox
  ↓
Repair once if needed
  ↓
Generate draft PR summary
```

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
