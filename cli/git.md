# Git — version control for code and text
# Use it to track changes, collaborate, and ship safely.

## 1) First‑time setup
- `git config --global user.name "Your Name"` — commit author name
- `git config --global user.email "you@example.com"` — commit author email
- `git config --global init.defaultBranch main` — new repos use `main`
- `git config --global pull.rebase true` — pull uses rebase
- `git config --global core.editor "code --wait"` — set editor

## 2) Create a new repo and push (ordered)
1) `git init` — create repo
2) `git add .` — stage all files
3) `git commit -m "Initial commit"` — first snapshot
4) `git branch -M main` — rename default branch
5) `git remote add origin git@github.com:USER/REPO.git` — add SSH remote
6) `git push -u origin main` — push + set upstream

## 3) Clone, update, build (ordered)
- `git clone git@github.com:ORG/REPO.git` — SSH clone
- `git clone https://github.com/ORG/REPO.git` — HTTPS clone
- `cd REPO`
- `git pull --rebase` — update cleanly
- `make -j$(nproc)` — build fast
- `sudo make install` — install (if needed)

## 4) Daily loop (edit → commit → push)
- `git status -sb` — short status + branch
- `git add <files>` — stage
- `git add -p` — stage by hunk
- `git commit -m "Short message"` — commit
- `git push` — upload

## 5) Branches + PRs
- `git switch -c feature/name` — new branch
- `git switch main` — switch branch
- `git switch -` — jump to previous branch
- `git merge main` — merge main into your branch
- `git rebase main` — replay your work on main
- `git push -u origin feature/name` — push branch
- `git push --force-with-lease` — safe force push after rebase

## 6) Inspect changes
- `git diff` — unstaged changes
- `git diff --staged` — staged changes
- `git diff --name-only` — list changed files
- `git log --oneline --graph --decorate --all` — compact history
- `git show <commit>` — details for a commit
- `git blame <file>` — who changed each line

## 7) Undo / fix mistakes
- `git restore <file>` — discard local changes
- `git restore --staged <file>` — unstage only
- `git commit --amend` — fix last commit
- `git reset --soft HEAD~1` — undo commit, keep staged
- `git reset --mixed HEAD~1` — undo commit, keep unstaged
- `git reset --hard HEAD~1` — undo commit, drop changes (danger)
- `git revert <commit>` — safe undo via new commit
- `git reflog` — recover lost commits

## 8) Stash
- `git stash push -m "wip"` — save work temporarily
- `git stash list` — list stashes
- `git stash apply` — apply without dropping
- `git stash pop` — apply + drop

## 9) Tags / releases
- `git tag v1.2.3` — lightweight tag
- `git tag -a v1.2.3 -m "release"` — annotated tag
- `git push origin v1.2.3` — push tag

## 10) Remotes
- `git remote -v` — show remotes
- `git remote set-url origin <url>` — change remote URL

## 11) Useful options
- `git fetch --prune` — remove deleted remote branches
- `git pull --ff-only` — fail if non‑fast‑forward
- `git clean -fd` — delete untracked files/dirs (danger)
- `git submodule update --init --recursive` — sync submodules
