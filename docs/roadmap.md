# Roadmap

## Phase 1: Demo repo and issue intake

- Prepare a small demo repository.
- Create sample issues: bug fix, test add, small feature.
- Parse issue goal, constraints, and acceptance criteria.

## Phase 2: Repository context

- Build repo map.
- Detect package manager, test command, and main source folders.
- Retrieve relevant files using lexical search and optional embeddings.

## Phase 3: Plan and patch

- Generate change plan and risk notes.
- Generate minimal patch.
- Limit changed files and avoid broad rewrites by default.

## Phase 4: Test and repair

- Run tests in a controlled environment.
- Parse failure logs.
- Attempt one repair loop.
- Produce final diff and PR summary.

## Phase 5: Interview package

- Add example issue-to-PR traces.
- Add PR summary examples.
- Add notes on context construction and safety limits.
