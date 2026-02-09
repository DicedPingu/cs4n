# github (git + gh) - cross-device GitHub workflow
# Use it to work from Pop!_OS, Android, and AI-assisted environments without breaking history.
# Canonical Git/GitHub CLI guide for this repo.

## 0) Fast terminal workflow (no IDE dependency)
- `gh repo clone OWNER/REPO && cd REPO`
- `git switch main && git pull --rebase --autostash`
- `git switch -c feature/<topic>`
- Edit files with terminal/editor of choice.
- `git add -p && git commit -m "feat: concise summary"`
- `git push -u origin feature/<topic>`
- `gh pr create --draft --fill`

## 1) Core strategy (works from every device)
- Keep `origin/main` as the source of truth.
- Always start by syncing before coding.
- Use short-lived feature branches, not direct commits to `main`.
- Keep separate SSH keys per device; never copy private keys between devices.

## 2) One-time setup on Pop!_OS
- `sudo apt update && sudo apt install -y git gh openssh-client` - install base tooling.
- `git config --global user.name "Your Name"`
- `git config --global user.email "you@example.com"`
- `git config --global init.defaultBranch main`
- `git config --global pull.rebase true`
- `gh auth login` - authenticate GitHub CLI.
- `gh auth setup-git` - configure git credential flow.

## 3) One-time setup on Android (Termux)
- `pkg update && pkg upgrade -y`
- `pkg install -y git gh openssh`
- `termux-setup-storage` - optional shared storage access.
- `git config --global user.name "Your Name"`
- `git config --global user.email "you@example.com"`
- `git config --global init.defaultBranch main`
- `git config --global pull.rebase true`
- `gh auth login` - authenticate from mobile shell.

## 4) SSH key model for multiple places
### Pop!_OS key
- `ssh-keygen -t ed25519 -a 100 -f ~/.ssh/id_ed25519_popos -C "you@popos"`
- `gh ssh-key add ~/.ssh/id_ed25519_popos.pub --title "popos-main"`

### Android key
- `ssh-keygen -t ed25519 -a 100 -f ~/.ssh/id_ed25519_android -C "you@android"`
- `gh ssh-key add ~/.ssh/id_ed25519_android.pub --title "android-termux"`

### Verify GitHub SSH auth
- `ssh -T git@github.com`

## 5) Create a repository
### New local project -> GitHub
- `mkdir myproj && cd myproj`
- `git init -b main`
- `git add . && git commit -m "Initial commit"`
- `gh repo create OWNER/REPO --private --source=. --remote=origin --push`

### Existing local repo -> attach remote
- `gh repo create OWNER/REPO --private --source=. --remote=origin`
- `git push -u origin main`

### Existing GitHub repo -> clone
- `gh repo clone OWNER/REPO`
- `gh repo clone OWNER/REPO -- --depth 1` - shallow option.

## 6) Update flow (every session, every device)
### Start work safely
- `git switch main`
- `git fetch origin --prune`
- `git pull --rebase --autostash`
- `git switch -c feature/<topic>`

### Publish your work
- `git add -p`
- `git commit -m "feat: concise summary"`
- `git push -u origin feature/<topic>`

### Keep branch updated while coding
- `git fetch origin --prune`
- `git rebase origin/main`
- `git push --force-with-lease`

### If rebase conflicts
- `git status`
- Resolve files, then `git add <resolved-files>`
- `git rebase --continue`
- `git rebase --abort` - cancel if needed.

## 7) Multi-device handoff pattern (Pop!_OS <-> Android <-> AI)
- Finish each session with a commit and push.
- Continue from another device with:
```bash
git fetch origin --prune
git switch feature/<topic>
git pull --rebase
```
- If you need temporary sync without final message, use `git commit -m "wip: ..."` and squash later.

## 8) AI-assisted workflow (Codex and Code Insiders++)
- Use AI changes on dedicated branches like `ai/codex/<topic>` or `ai/codeinsiders/<topic>`.
- On Pop!_OS, open the repo in Insiders with `code-insiders .` and run Git commands in its integrated terminal.
- Before asking AI to edit, run `git status -sb` and ensure a clean base.
- After AI edits, review with:
```bash
git diff --staged
git log --oneline --graph --decorate -20
```
- Open PR early with `gh pr create --draft --fill` and iterate.

## 9) Pull requests, issues, releases, and CI
- `gh pr create --fill` - open PR.
- `gh pr checks <number>` - check CI.
- `gh pr merge <number> --squash` - merge cleanly.
- `gh issue create --title "..." --body "..." --label bug`
- `gh workflow run ci.yml`
- `gh run view <run-id> --log`
- `gh release create vX.Y.Z --notes-file CHANGELOG.md`

## 10) Safety guardrails
- Prefer `git revert` over `git reset --hard` on shared branches.
- Use `git push --force-with-lease` instead of `--force`.
- Never reuse one private SSH key across multiple devices.

## 11) Version and release line
- Local checks: `git --version && gh --version`
- Upstream release snapshot: Git `2.53.0`, gh `v2.86.0`.
