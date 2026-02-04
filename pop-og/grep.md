# grep Quicksheet
Search text in files.

## basics
- `grep 'pattern' file`
  - What it does: Prints lines matching pattern.
  - When to use it: Quick searches in one file.
- `grep -R 'pattern' dir/`
  - What it does: Recursively searches a directory.
  - When to use it: Codebase-wide lookups.
- `grep -n 'pattern' file`
  - What it does: Shows matching lines with line numbers.
  - When to use it: Pinpointing where a match lives.
- `grep -i 'pattern' file`
  - What it does: Case-insensitive match.
  - When to use it: Loose matching.

## useful filters
- `grep -v 'pattern' file`
  - What it does: Prints lines that do NOT match.
  - When to use it: Excluding noise.
- `grep -w 'word' file`
  - What it does: Matches whole words only.
  - When to use it: Avoiding partial matches.
- `grep -E 'foo|bar' file`
  - What it does: Uses extended regex for alternation.
  - When to use it: Multiple patterns in one pass.
- `grep -F 'literal' file`
  - What it does: Treats pattern as a fixed string.
  - When to use it: Searching for regex-heavy text.

## context and counts
- `grep -C 2 'pattern' file`
  - What it does: Shows 2 lines of context around matches.
  - When to use it: Understanding surrounding content.
- `grep -A 3 -B 1 'pattern' file`
  - What it does: Shows custom before/after context.
  - When to use it: Tighter context windows.
- `grep -c 'pattern' file`
  - What it does: Counts matches per file.
  - When to use it: Quick frequency checks.
- `grep -l 'pattern' *.log`
  - What it does: Lists files with at least one match.
  - When to use it: Finding which files matter.
- `grep -m 1 'pattern' file`
  - What it does: Stops after the first match.
  - When to use it: Fast checks in large files.
