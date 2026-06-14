# Data Model

## Core tables

### coding_tasks

| Field | Purpose |
|---|---|
| id | Task id |
| issue_url | Source issue URL |
| title | Issue title |
| body | Issue body |
| status | new, mapped, planned, tested, summarized |
| created_at | Created time |

### acceptance_criteria

| Field | Purpose |
|---|---|
| id | Criteria id |
| task_id | Parent task |
| text | Criteria text |
| status | pending, satisfied, unclear |

### repo_files

| Field | Purpose |
|---|---|
| id | File record id |
| task_id | Parent task |
| path | Repository path |
| file_type | source, test, config, docs |
| reason | Why this file matters |

### change_plans

| Field | Purpose |
|---|---|
| id | Plan id |
| task_id | Parent task |
| summary | Short plan |
| risk_note | What to review carefully |

### test_runs

| Field | Purpose |
|---|---|
| id | Test run id |
| task_id | Parent task |
| command | Command used |
| result | pass, fail, skipped |
| output_summary | Short output summary |

### review_summaries

| Field | Purpose |
|---|---|
| id | Summary id |
| task_id | Parent task |
| changed_files | Files touched or proposed |
| tests | Test summary |
| reviewer_notes | What a human should check |

## MVP rule

The record should make the work reviewable even if the first version is not fully automated.
