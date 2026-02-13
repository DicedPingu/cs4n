# GitHub Guide (Practical, Beginner-Friendly)
Use this file when you are new to git and want the exact command order for normal work.

## 1) One-time setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
git config --global pull.rebase true
gh auth login
gh auth setup-git
```

## 2) Get a repo on your machine
If the repo already exists on GitHub:
```bash
gh repo clone OWNER/REPO
cd REPO
```

If you already have a folder locally and want to publish it:
```bash
cd my-project
git init -b main
git add .
git commit -m "Initial commit"
gh repo create OWNER/REPO --private --source=. --remote=origin --push
```

## 3) Daily workflow (copy this every time)
Start work:
```bash
git switch main
git pull --rebase --autostash
git switch -c feature/short-topic
```

Save work:
```bash
git status
git add -p
git commit -m "feat: short clear message"
git push -u origin feature/short-topic
```

Open a Pull Request:
```bash
gh pr create --fill
```

## 4) Continue work on the same branch tomorrow
```bash
git switch feature/short-topic
git fetch origin --prune
git rebase origin/main
git push --force-with-lease
```

## 5) Pull and push explained simply
- `git pull` = get new commits from GitHub and apply them locally.
- `git push` = send your local commits to GitHub.
- Pull before coding, push after each finished chunk.

## 6) Read status fast
```bash
git status -sb
git log --oneline --graph --decorate -20
```

## 7) Common "I'm stuck" fixes
See changed files:
```bash
git status
git diff
```

Undo unstaged edits in one file:
```bash
git restore path/to/file
```

Unstage a file:
```bash
git restore --staged path/to/file
```

Abort a bad rebase:
```bash
git rebase --abort
```

## 8) Safe habits
- Never commit directly to `main`.
- Prefer `git revert` over history rewrite on shared branches.
- If you must force push, use `--force-with-lease`, never plain `--force`.
- Commit small, meaningful chunks.

## 9) Useful extras (`++`)
Quick review before commit:
```bash
git diff --staged
```

Sync and clean deleted remote branches:
```bash
git fetch --prune
```

Create issue / check PR:
```bash
gh issue create --title "..." --body "..."
gh pr checks <number>
```
