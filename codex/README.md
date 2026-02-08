# Codex Control Kit
This folder is your control surface for getting more predictable, higher-quality Codex outputs.

## Files
- `codex/request-template.md` - ask once, get complete execution.
- `codex/control-profiles.md` - selectable behavior profiles by task type.
- `codex/review-checklist.md` - quality and risk checks before accepting changes.
- `codex/workflow-rules.md` - repo-specific execution rules for consistent behavior.
- `codex/extensions-packages-repos.md` - recommended editor extensions, packages, and repo/PPA strategy.
- `codex/version-sources.md` - auditable upstream release links and snapshot versions.

## Recommended usage order
1. Pick a profile from `codex/control-profiles.md`.
2. Fill request content using `codex/request-template.md`.
3. Add project rules in `codex/workflow-rules.md`.
4. Use `codex/review-checklist.md` on every non-trivial change.

## Optional enforcement
- Mirror the rules you care about into your root `AGENTS.md` so they are always loaded.

