# Control Profiles
Pick one profile and include it in your prompt.

## Profile A - Fast Patch
Use when: small bug/docs fix needed quickly.
- Keep edits minimal and localized.
- Prefer smallest safe change over refactor.
- Run focused validation only.

## Profile B - Production Safe
Use when: reliability and regressions matter.
- Read all related files before editing.
- Add or update tests for behavior changes.
- Explain tradeoffs and failure modes.
- Avoid risky commands and broad rewrites.

## Profile C - Deep Refactor
Use when: structure and maintainability are the priority.
- Reorganize modules for coherence.
- Preserve behavior unless explicitly approved to change.
- Leave migration notes in changed docs.
- Validate full affected workflow, not only unit tests.

## Profile D - Reviewer Mode
Use when: you want a strict code review first.
- Prioritize findings by severity.
- Include file references for each finding.
- Suggest concrete patches, not just comments.
- State residual risk and missing tests.

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
