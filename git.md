# Git + GitHub (Practical Workflow Cheatsheet)

## 1) First‑time setup (one‑time)
- `git config --global user.name "Your Name"`
  - Sets commit author name.
- `git config --global user.email "you@example.com"`
  - Sets commit author email.
- `git config --global init.defaultBranch main`
  - New repos default to `main`.
- `git config --global pull.rebase true`
  - Makes `git pull` rebase by default (cleaner history).

## 2) Create a new repo and push it to GitHub (ordered)
1) `mkdir myrepo && cd myrepo`
2) `git init`
3) `git add .`
4) `git commit -m "Initial commit"`
5) `git branch -M main`
6) `git remote add origin git@github.com:USER/REPO.git`
7) `git push -u origin main`

## 3) Clone, build, update (ordered)
- `git clone git@github.com:ORG/REPO.git`
- `cd REPO`
- `git pull`
- Build/update (common pattern):
  - `make -j$(nproc)`
  - `sudo make install`

## 4) Daily loop (edit → commit → push)
1) `git status`
2) `git add <files>` (or `git add -p` for clean commits)
3) `git commit -m "Short message"`
4) `git push`

## 5) Branches + PRs (ordered)
- `git switch -c feature/short-name`
- Work + commit
- `git push -u origin feature/short-name`
- Open PR in GitHub
- After merge: `git switch main && git pull --rebase`

## 6) Syncing + keeping clean history
- `git fetch` — update remote refs only
- `git pull --rebase` — replay local commits on latest remote
- `git rebase main` — rebase your branch onto `main`
- `git merge main` — merge `main` into your branch
- `git push --force-with-lease` — safe force push after rebase

## 7) Common commands + useful options
- `git status -sb`
  - Short, branch‑aware status.
- `git log --oneline --graph --decorate --all`
  - Compact visual history.
- `git diff`
  - Unstaged changes.
- `git diff --staged`
  - Staged changes.
- `git add -p`
  - Stage hunks interactively.
- `git restore <file>`
  - Discard local changes in file.
- `git restore --staged <file>`
  - Unstage but keep local changes.
- `git stash push -m "wip"`
  - Save work temporarily.
- `git stash pop`
  - Restore stashed work.

## 8) Undo / fix mistakes
- `git reset --soft HEAD~1`
  - Undo last commit, keep changes staged.
- `git reset --mixed HEAD~1`
  - Undo last commit, keep changes unstaged.
- `git reset --hard HEAD~1`
  - Undo last commit and discard changes (danger).
- `git revert <commit>`
  - Create a new commit that undoes a commit.

## 9) Tags + releases
- `git tag v1.2.3`
- `git push origin v1.2.3`

## 10) GitHub CLI (gh) quick hits
- `gh auth login`
- `gh repo create <name> --public --source=. --remote=origin`
- `gh pr create --fill`
- `gh pr view --web`
- `gh pr checkout <PR_NUMBER>`
- `gh issue list`

## 11) Misc + advanced
- `git blame <file>`
  - Who changed what line.
- `git clean -fd`
  - Remove untracked files/dirs (danger).
- `git submodule update --init --recursive`
  - Sync submodules.
- `git config --global core.autocrlf input`
  - Normalize line endings (Linux/macOS).

