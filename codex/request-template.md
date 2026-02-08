# Request Template
Use this prompt shape when you want controlled execution quality.

## Task
- Goal: <what must be true at the end>
- Scope: <files/folders allowed>
- Out of scope: <what to avoid>

## Constraints
- Style: <coding/doc style constraints>
- Safety: <no destructive commands, migration constraints, etc.>
- Performance: <acceptable complexity/runtime>

## Execution requirements
- Inspect all impacted files before edits.
- Implement directly; do not stop at planning.
- Validate with tests or command checks.
- Report exact files changed and why.

## Output format
- First: outcome summary (2-4 lines).
- Then: numbered change list with file references.
- Then: validation commands and results.
- Last: optional next steps (max 3).

## Strictness toggles
- Depth: `quick | normal | deep`
- Risk tolerance: `low | medium | high`
- Autonomy: `guided | autonomous`

