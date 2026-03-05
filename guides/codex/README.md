# Codex Control Kit
Operational templates for stronger prompt quality, safer execution, and reliable reviews.

## Files and locations
- `guides/codex/request-template.md` - high-signal task request format.
- `guides/codex/control-profiles.md` - profile presets by task type.
- `guides/codex/review-checklist.md` - acceptance checklist for changes.
- `guides/codex/workflow-rules.md` - workflow guardrails and execution rules.
- `guides/codex/extensions-packages-repos.md` - editor/tooling package recommendations.
- `guides/codex/version-sources.md` - upstream reference links and snapshot notes.

## Recommended order
1. Pick a profile in `control-profiles.md`.
2. Fill request details in `request-template.md`.
3. Validate results with `review-checklist.md`.
4. Keep `workflow-rules.md` near active projects.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `rg -n 'TODO|FIXME' .` | Quickly find outstanding work items |
| `rg -n '^## ' guides/codex` | Audit codex section structure |
| `git diff --stat` | High-level size of current changes |
| `git diff -- guides/codex` | Inspect codex-only edits |
| `git log --oneline --decorate -n 15` | Quick recent-history review |
| `gh pr view --web` | Open current branch PR in browser |
| `gh issue list --limit 20` | Pull current issue queue |
| `jq -r '.[] | .name' package.json` | Extract JSON values during review workflows |
| `xargs -I{} echo {} < file.txt` | Apply quick command fan-out for templated inputs |
| `find . -type f -name 'AGENTS.md'` | Locate all agent policy files |
| `sed -n '1,120p' guides/codex/review-checklist.md` | Preview checklist without opening editor |
| `python -m pytest -q` | Fast correctness signal for Python repos |
