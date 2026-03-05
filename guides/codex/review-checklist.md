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
