# gh - GitHub CLI for repos, pull requests, issues, and CI
# Use it to run GitHub workflows from terminal without context switching.

## Authentication and setup
- `gh auth login` - authenticate with browser/token flow.
- `gh auth status` - show active account and scopes.
- `gh auth setup-git` - wire git credentials through gh.

## Repo lifecycle
- `gh repo create <name> --private --source=. --remote=origin` - create and connect local repo.
- `gh repo clone OWNER/REPO` - clone remote repository.
- `gh repo set-default OWNER/REPO` - set default target for subsequent commands.
- `gh repo view --web` - open repo quickly in browser.

## Pull request flow (daily)
- `gh pr create --fill` - open PR from commits using template defaults.
- `gh pr create --draft` - open draft PR.
- `gh pr status` - see your open PRs/reviews.
- `gh pr view <number> --web` - inspect PR details.
- `gh pr checkout <number>` - fetch and checkout PR branch.
- `gh pr merge <number> --squash` - merge with squash strategy.

## Issues and release operations
- `gh issue list --assignee @me` - your assigned issues.
- `gh issue create --title "..." --body "..." --label bug` - create structured issue.
- `gh release create vX.Y.Z --notes-file CHANGELOG.md` - publish release from changelog.
- `gh release list` - inspect published releases.

## Actions and automation
- `gh workflow list` - list available workflows.
- `gh workflow run ci.yml` - trigger workflow manually.
- `gh run list --limit 10` - recent workflow runs.
- `gh run view <run-id> --log` - inspect logs.
- `gh api repos/OWNER/REPO/pulls --jq '.[].title'` - script via GitHub API.

## Version and release line
- Local check: `gh --version`
- Upstream release snapshot: gh `v2.86.0`.

