# Workflow Rules for Codex
Paste or adapt these into root `AGENTS.md` for always-on behavior.

## Editing rules
- Read all relevant files before editing.
- Keep related information close together.
- Prefer command sequences in real execution order.
- Include safe variant before destructive command.

## Quality rules
- For docs: include "when to use", "main flow", and "version check".
- For code: include tests for logic changes.
- Avoid speculative claims; verify versioned info from official sources.

## Communication rules
- Summarize outcome first.
- List changed files with concise rationale.
- If blocked, state blocker and best fallback.

## Repo hygiene
- Do not revert unrelated user changes.
- Keep commits focused by concern.
- Use ASCII unless file already requires Unicode.

## Multi-device Git rules (Pop!_OS, Android, AI)
- Sync first on every device: `git fetch origin --prune` then `git pull --rebase`.
- Commit and push before switching devices.
- Keep separate SSH keys per device and rotate compromised keys immediately.

## AI branch rules (Codex, Code Insiders++)
- Run AI edits only on dedicated branches (`ai/<tool>/<topic>`).
- Require clean working tree before AI edits unless explicitly doing refactors.
- Open draft PRs early for AI-generated changes and review diffs before merge.

