# GitHub Guide (Practical + Explained)
Use this when you are new to git. Every workflow step includes what the command and flags actually do.

## 1) One-time setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
git config --global pull.rebase true
gh auth login
gh auth setup-git
```
What this does:
- `git config --global ...`: writes settings into your global git config (`~/.gitconfig`) for all repos.
- `user.name` / `user.email`: identity shown on commits.
- `init.defaultBranch main`: new repos start on `main`.
- `pull.rebase true`: `git pull` rebases your commits on top of remote changes instead of creating extra merge commits.
- `gh auth login`: signs GitHub CLI in.
- `gh auth setup-git`: lets git reuse GitHub CLI auth for HTTPS operations.

## 2) Get a repo on your machine
If repo exists on GitHub:
```bash
gh repo clone OWNER/REPO
cd REPO
```
What this does:
- `gh repo clone OWNER/REPO`: clones a GitHub repo using `owner/repo`.
- `cd REPO`: moves into that folder so future git commands target that repo.

If project is local and you want to publish it:
```bash
cd my-project
git init -b main
git add .
git commit -m "Initial commit"
gh repo create OWNER/REPO --private --source=. --remote=origin --push
```
What this does:
- `git init -b main`: turns folder into a git repo and starts on `main`.
- `git add .`: stages all current files.
- `git commit -m "..."`: saves a snapshot with a message.
- `gh repo create ...`: creates GitHub repo and links/pushes local repo.

Option breakdown for `gh repo create`:
- `--private`: repo is private.
- `--source=.`: use current folder as source.
- `--remote=origin`: name remote `origin`.
- `--push`: push local commits immediately.

## 3) Daily workflow (do this every work session)
Start work:
```bash
git switch main
git pull --rebase --autostash
git switch -c feature/short-topic
```
What this does:
- `git switch main`: moves to `main`.
- `git pull --rebase --autostash`: downloads remote commits and reapplies your local work cleanly.
- `git switch -c feature/short-topic`: creates and switches to a new branch.

Option breakdown:
- `--rebase`: replay local commits on top of remote branch.
- `--autostash`: temporarily stash dirty changes during pull/rebase and restore after.
- `-c`: create a new branch while switching.

Save and publish work:
```bash
git status
git add -p
git commit -m "feat: short clear message"
git push -u origin feature/short-topic
```
What this does:
- `git status`: shows changed/staged/untracked files.
- `git add -p`: stage changes interactively hunk-by-hunk.
- `git commit -m "..."`: records staged changes.
- `git push -u origin feature/short-topic`: uploads branch and sets upstream tracking.

Option breakdown:
- `-p` (`git add`): patch mode (pick exact pieces).
- `-m` (`git commit`): commit message inline.
- `-u` (`git push`): set upstream so later `git push`/`git pull` works without full branch name.

Open Pull Request:
```bash
gh pr create --fill
```
What this does:
- Opens a PR from your current branch to default base branch.
- `--fill`: auto-fills title/body from commits.

## 4) Continue same branch later
```bash
git switch feature/short-topic
git fetch origin --prune
git rebase origin/main
git push --force-with-lease
```
What this does:
- `git fetch origin --prune`: updates remote refs and deletes stale remote-tracking branches.
- `git rebase origin/main`: puts your branch commits on latest `main`.
- `git push --force-with-lease`: updates remote branch after rebase safely.

Option breakdown:
- `--prune`: remove local refs for remote branches that were deleted.
- `--force-with-lease`: force push only if remote branch is still what you expect.

## 5) Pull vs push (simple)
- `git pull`: bring remote commits down into local branch.
- `git push`: send local commits up to remote branch.
- Rule: pull before coding, push after each finished chunk.

## 6) Check state quickly
```bash
git status -sb
git log --oneline --graph --decorate -20
```
What this does:
- `git status -sb`: short status + branch line.
- `git log ...`: compact visual commit graph.

Option breakdown:
- `-s`: short format.
- `-b`: include branch and tracking info.
- `--oneline`: one line per commit.
- `--graph`: ASCII graph of branches/merges.
- `--decorate`: show branch/tag names.
- `-20`: show last 20 commits.

## 7) "I'm stuck" fixes
See changes:
```bash
git status
git diff
```
- `git diff`: show unstaged changes.

Discard unstaged changes in one file:
```bash
git restore path/to/file
```
- Restores file from current commit (`HEAD`).

Unstage a file:
```bash
git restore --staged path/to/file
```
- Removes file from staging area, keeps working copy edits.

Abort broken rebase:
```bash
git rebase --abort
```
- Returns branch to pre-rebase state.

## 8) Safe habits
- Never commit directly to `main`.
- Prefer `git revert` over rewriting shared history.
- If you must force push, use `--force-with-lease`.
- Make small commits with clear messages.

## 9) Useful extras (`++`)
Review staged changes before commit:
```bash
git diff --staged
```
- `--staged`: compare staged changes vs last commit.

Clean stale remote tracking refs:
```bash
git fetch --prune
```

Create issue / check PR CI:
```bash
gh issue create --title "..." --body "..."
gh pr checks <number>
```
Option breakdown:
- `--title`: issue title.
- `--body`: issue description.
