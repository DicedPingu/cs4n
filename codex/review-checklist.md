# Review Checklist
Run this before accepting a Codex-generated change.

## Correctness
- Does behavior match the requested outcome?
- Are edge cases handled?
- Are destructive operations guarded?

## Scope control
- Only intended files changed.
- No unrelated formatting churn.
- No accidental API/CLI breaking change.

## Validation
- Relevant tests executed.
- Build/lint commands pass.
- New docs/examples run as written.

## Security and safety
- No leaked secrets/tokens.
- No insecure defaults introduced.
- Dependency updates are intentional.

## Documentation quality
- Commands are copy/paste safe.
- Steps are ordered by real usage flow.
- Alternatives and failure recovery are included.

