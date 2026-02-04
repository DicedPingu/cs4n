# gh — GitHub CLI for repos, PRs, issues, releases
# Use it to do GitHub work without leaving the terminal.

## 1) Auth
- `gh auth login` — sign in
- `gh auth status` — show active account
- `gh auth logout` — sign out
- `gh auth setup-git` — configure git to use gh auth

## 2) Create repo (ordered)
- `gh repo create <name> --public --source=. --remote=origin` — create + add remote
- `gh repo create <name> --private --source=. --remote=origin` — private repo
- `git push -u origin main` — first push

## 3) Clone / open
- `gh repo clone OWNER/REPO` — clone
- `gh repo clone OWNER/REPO -- --depth 1` — shallow clone
- `gh repo view --web` — open in browser
- `gh repo set-default` — set default repo for gh

## 4) PR workflow
- `gh pr create --fill` — create PR from commits
- `gh pr create --draft` — draft PR
- `gh pr create --reviewer @user --label bug` — add metadata
- `gh pr status` — list your PRs
- `gh pr view --web` — open PR in browser
- `gh pr checkout <PR>` — checkout PR locally
- `gh pr merge <PR> --squash|--merge|--rebase` — merge styles

## 5) Issues
- `gh issue list` — list issues
- `gh issue create --title "..." --body "..."` — new issue
- `gh issue create --label bug --assignee @me` — set metadata
- `gh issue view <ID> --web` — open in browser

## 6) Releases
- `gh release create vX.Y.Z --notes "..."` — publish release
- `gh release list` — list releases
- `gh release view vX.Y.Z --web` — open in browser

## 7) Actions / CI
- `gh workflow list` — workflows
- `gh workflow run <workflow.yml>` — trigger run
- `gh run list` — recent runs
- `gh run view <ID> --log` — logs
- `gh run watch <ID>` — stream run status

## 8) Useful options
- `--web` — open in browser
- `--json <fields> --jq <filter>` — scriptable output

## 9) Misc + advanced
- `gh gist create <file>` — create a gist
- `gh repo fork OWNER/REPO --clone` — fork + clone
- `gh api <path>` — raw GitHub API
