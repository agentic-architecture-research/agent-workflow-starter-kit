# atomic-task-graph.md

## Atomic Task Rule

An atomic task is a bounded execution unit. The executor should not make workflow-level, scope-level, or design-level decisions while executing it.

Each executable task should define or tightly imply:

- Objective boundary: what exact operation is being performed.
- Input boundary: what files, schemas, endpoints, or artifacts are in scope.
- Authority boundary: what the executor may change or call.
- Evaluation boundary: what counts as done.
- Stop boundary: when the executor should stop.

## Task Graph

### Foundation

- T001 Create repository-specific knowledge index
  - Depends on: none
  - Objective: Populate `agent/knowledge/index.md` with the repo's canonical files, areas, and context routes.
  - Inputs: repository tree, existing docs, existing code structure
  - Authority: update `agent/knowledge/index.md` only unless obvious setup notes belong in progress files
  - Validation: index identifies canonical artifacts, major repo areas, and stale/unknown areas
  - Stop: stop after the initial index is useful enough to route future tasks

## Compact Adjacency View

```text
T001 ->
```
