# touch Quicksheet
Create files or update timestamps.

## basics
- `touch file.txt`
  - What it does: Creates the file if it doesn't exist.
  - When to use it: Quick placeholder files.
- `touch file.txt other.txt`
  - What it does: Creates or updates multiple files.
  - When to use it: Batch timestamp updates.

## timestamp control
- `touch -a file.txt`
  - What it does: Updates access time only.
  - When to use it: Preserve modify time.
- `touch -m file.txt`
  - What it does: Updates modify time only.
  - When to use it: Bump a file for rebuilds.
- `touch -t 202501291230 file.txt`
  - What it does: Sets a specific timestamp (YYYYMMDDhhmm).
  - When to use it: Repro builds or tests.

## reference
- `touch -r source.txt target.txt`
  - What it does: Copies timestamps from another file.
  - When to use it: Keep file times aligned.
