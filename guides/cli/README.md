# CLI Guides
Everyday terminal productivity and repository command flows.

## Files and locations
- `guides/cli/github.md` - practical Git + GitHub CLI workflow.
- `guides/cli/rg.md` - high-speed searching with ripgrep.
- `guides/cli/tmux.md` - persistent terminal sessions.
- `guides/cli/wget.md` - resilient downloads.

## Recommended order
1. `github.md`
2. `rg.md`
3. `tmux.md`
4. `wget.md`

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `git status -sb` | Compact branch and change overview |
| `git switch -c feat/<name>` | Create and switch to feature branch |
| `git add -p` | Stage hunks interactively |
| `git commit -m '<message>'` | Commit staged changes |
| `gh pr create --fill` | Open pull request from current branch |
| `gh pr checks` | View PR checks status quickly |
| `rg -n '<pattern>' .` | Search with line numbers in current tree |
| `rg -n --hidden --glob '!.git' '<pattern>'` | Include hidden files but skip git internals |
| `tmux new -s dev` | Start a named tmux session |
| `tmux attach -t dev` | Reattach to existing session |
| `wget -c '<url>'` | Continue interrupted downloads |
| `wget --mirror --convert-links '<url>'` | Mirror site content for offline browsing |
