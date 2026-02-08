# Git - distributed version control
# Use it to track changes safely, collaborate on branches, and recover from mistakes.

## One-time setup
- `git config --global user.name "Your Name"`
- `git config --global user.email "you@example.com"`
- `git config --global init.defaultBranch main`
- `git config --global pull.rebase true`
- `git config --global rerere.enabled true` - remember conflict resolutions.

## Daily branch workflow
- `git switch -c feature/topic` - create and move to feature branch.
- `git status -sb` - concise branch/status overview.
- `git add -p` - stage only intended hunks.
- `git commit -m "feat: short message"` - commit scoped change.
- `git fetch origin --prune` - update remote refs.
- `git rebase origin/main` - keep branch current.
- `git push -u origin feature/topic` - publish branch.

## Reviewing history and changes
- `git diff` - unstaged changes.
- `git diff --staged` - staged changes.
- `git log --oneline --graph --decorate --all` - branch graph view.
- `git show <commit>` - full patch for one commit.
- `git blame -L 20,60 path/file` - line-level ownership.

## Recovery and safe undo
- `git restore <file>` - discard local unstaged changes.
- `git restore --staged <file>` - unstage while keeping file edits.
- `git commit --amend --no-edit` - append staged fixes to last commit.
- `git revert <commit>` - undo via a new commit (safe on shared branches).
- `git reflog` - recover lost commits/branch tips.

## Tag and release basics
- `git tag -a v1.2.3 -m "release 1.2.3"`
- `git push origin v1.2.3`

## Dangerous commands (use intentionally)
- `git reset --hard <rev>` - discards tracked changes.
- `git clean -fd` - removes untracked files/directories.
- `git push --force-with-lease` - force update with safety check.

## Version and release line
- Local check: `git --version`
- Upstream release snapshot: Git `2.53.0`.

