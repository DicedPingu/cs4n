# find Quicksheet
Find files with filters.

## name and path
- `find . -name '*.log'`
  - What it does: Finds files by exact name pattern (case-sensitive).
  - When to use it: Targeted searches.
- `find . -iname '*.log'`
  - What it does: Finds files by name pattern (case-insensitive).
  - When to use it: When case is unknown.
- `find . -path './node_modules' -prune -o -name '*.js' -print`
  - What it does: Skips node_modules, searches for JS files elsewhere.
  - When to use it: Large repos with vendor dirs.

## time and size
- `find . -type f -size +10M`
  - What it does: Finds files larger than 10 MB.
  - When to use it: Disk cleanup.
- `find . -type f -mtime -7`
  - What it does: Finds files modified in the last 7 days.
  - When to use it: Recent changes.
- `find . -type f -mmin -60`
  - What it does: Finds files modified in the last hour.
  - When to use it: Debugging recent writes.

## type and permissions
- `find . -type d`
  - What it does: Finds directories only.
  - When to use it: Folder audits.
- `find . -type f -perm -u+x`
  - What it does: Finds executable files.
  - When to use it: Script discovery.
- `find . -empty`
  - What it does: Finds empty files and dirs.
  - When to use it: Cleanup pass.

## executing actions
- `find . -type f -name '*.tmp' -delete`
  - What it does: Deletes matching files.
  - When to use it: Safe cleanup after a dry run.
- `find . -type f -name '*.log' -exec wc -l {} \;`
  - What it does: Runs a command per match.
  - When to use it: Simple per-file actions.
- `find . -type f -print0 | xargs -0 grep -n 'TODO'`
  - What it does: Searches matches safely with spaces in names.
  - When to use it: Batch processing.
