# Knowledge Index

This file helps agents decide what context to load before planning or execution.

It is advisory. Code, verified behavior, and canonical ledgers override this index when they disagree.

## Canonical Artifacts

| Artifact | Purpose | Authority |
|---|---|---|
| `plan.md` | Product constraints, phases, MVP cut | Product planning source |
| `atomic-task-graph.md` | Human-readable dependency graph | Planning reference |
| `tasks.json` | Machine-readable task ledger | Canonical task status and task contracts |
| `agent/progress/task-status.md` | Human-readable task status | Derived/working view |
| `agent/progress/session-notes.md` | Handoff and decisions | Supporting log |
| `agent/progress/change-log.md` | Append-only implementation log | Supporting log |
| `agent/progress/blockers.md` | Known blockers | Supporting log |
| `agent/feedback/issue-index.md` | Feedback backlog | Canonical issue-level feedback status |

## Repository Areas

Update this after inspecting the target repo.

| Area | Files / Directories | Notes | Confidence |
|---|---|---|---|
| TODO | TODO | TODO | low |

## Context Routes

Use these routes to avoid broad rediscovery.

| Task Type | Read First | Then Read | Avoid Unless Needed |
|---|---|---|---|
| New implementation task | `tasks.json`, `agent/progress/task-status.md`, this index | Files in task `inputs` and `write_scope` | unrelated feature folders |
| Feedback intake | `agent/feedback/issue-index.md`, this index | Relevant existing issue folders | main task ledger unless mapping to main tasks |
| Feedback resolution | issue folder `tasks.json`, `task-status.md`, this index | code in issue `files_expected` | unrelated issue folders |
| Architecture question | `plan.md`, `atomic-task-graph.md`, this index | manager starter prompts | product code unless needed |

## Prior Learnings

Record reusable implementation facts here.

- TODO

## Assumptions And Uncertainty

Record context that future agents should verify before relying on it.

- TODO

## Staleness Checks

Before trusting this index, check:

- Has the file tree changed substantially since the last update?
- Do task write scopes reference files that no longer exist?
- Do progress notes mention architecture changes not reflected here?
- Did a recent task add or move a canonical module?

## Last Updated

- TODO: date/time, agent, summary
