# GitHub CLI (gh) (Practical Workflow Cheatsheet)

## 1) First‑time setup (one‑time)
- `gh auth login`
  - Authenticates the CLI.
- `gh auth status`
  - Verify which account is active.
- `gh auth logout`
  - Switch accounts or clear auth.

## 2) Create a repo from a local folder (ordered)
1) `gh repo create <name> --public --source=. --remote=origin`
2) `git push -u origin main`

## 3) Clone and open (ordered)
- `gh repo clone OWNER/REPO`
- `cd REPO`
- `gh repo view --web`

## 4) PR workflow (ordered)
- `gh pr create --fill`
- `gh pr status`
- `gh pr view --web`
- `gh pr checkout <PR_NUMBER>`
- `gh pr merge <PR_NUMBER> --squash | --merge | --rebase`

## 5) Issues
- `gh issue list`
- `gh issue create --title "..." --body "..."`
- `gh issue view <NUMBER> --web`

## 6) Releases
- `gh release create vX.Y.Z --notes "..."`
- `gh release list`
- `gh release view vX.Y.Z --web`

## 7) Actions / CI
- `gh workflow list`
- `gh workflow run <workflow.yml>`
- `gh run list`
- `gh run view <RUN_ID> --log`

## 8) Useful options
- `--web` — open in browser
- `--json <fields>` + `--jq <filter>` — scripting

## 9) Misc + advanced
- `gh gist create <file>`
- `gh repo fork OWNER/REPO`
