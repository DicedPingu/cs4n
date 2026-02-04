# ls Quicksheet
List files and directories.

## everyday use
- `ls`
  - What it does: Lists files and directories.
  - When to use it: Quick view of a folder.
- `ls -a`
  - What it does: Shows hidden files (dotfiles).
  - When to use it: Inspecting config-heavy dirs.
- `ls -la`
  - What it does: Long listing, including hidden files.
  - When to use it: File details and permissions.
- `ls -lh`
  - What it does: Human-readable sizes.
  - When to use it: Understanding file sizes fast.

## sorting and grouping
- `ls -lt`
  - What it does: Sorts by modified time (newest first).
  - When to use it: Finding recent changes.
- `ls -ltr`
  - What it does: Sorts by time, oldest first.
  - When to use it: Seeing changes in order.
- `ls -S`
  - What it does: Sorts by size (largest first).
  - When to use it: Finding big files.
- `ls -1`
  - What it does: One entry per line.
  - When to use it: Piping into other commands.

## handy flags
- `ls -d */`
  - What it does: Lists directories only.
  - When to use it: Quick folder-only scan.
- `ls -p`
  - What it does: Appends `/` to directories.
  - When to use it: Distinguishing types at a glance.
- `ls -R`
  - What it does: Recursively lists subdirectories.
  - When to use it: Small trees; avoid on huge dirs.
