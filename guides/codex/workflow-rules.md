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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `git init` | Create an empty Git repository |
| `git clone https://example.com/repo.git` | Clone a remote Git repository from the internet |
| `git status` | View the status of the local repository |
| `git add [-A\|--all]` | Stage all changes for a commit |
| `git commit [-m\|--message] message_text` | Commit changes to version history |
| `git push` | Push local commits to a remote repository |
| `git pull` | Pull any changes made to a remote |
| `git reset --hard; git clean [-f\|--force]` | Reset everything the way it was in the latest commit |
| `git --help` | Show command usage and option reference |
| `man git` | Open the full manual page |
| `whatis git` | Print one-line command description |
| `type -a git` | Show how the shell resolves the command path |
| `command -v git` | Print executable path used by current shell |
| `tldr git` | Show concise command examples |
| `apropos git` | Search manual database for related commands |
| `git --version` | Print local tool version |
| `gh repo clone owner/repository` | Clone a GitHub repository locally |
| `gh issue [new\|create]` | Create a new issue |
| `gh issue [ls\|list]` | View and filter the open issues of the current repository |
| `gh issue view [-w\|--web] issue_number\|url` | View an issue in the default web browser |
