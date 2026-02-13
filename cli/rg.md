# rg (ripgrep) - fast recursive code search
Use it as your default text search tool in repositories.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## High-signal basics
- `rg "term"` - recursive search in current directory.
- `rg -n "term" path/` - include line numbers in selected path.
- `rg -i "term"` - case-insensitive.
- `rg -F "literal.string"` - literal matching, no regex parsing.

## File scope control
- `rg -g "*.py" "term"` - include only matching globs.
- `rg -g "!*.lock" "term"` - exclude lock files.
- `rg --hidden "term"` - include hidden files.
- `rg -uu "term"` - include ignored + hidden files.

## Output shaping for workflows
- `rg -l "TODO"` - filenames only.
- `rg -C 2 "panic"` - include context.
- `rg --json "term"` - machine-readable output.
- `rg "term" | fzf` - interactive narrowing.

## When grep is still useful
- Use `grep` for POSIX-only environments where `rg` is not installed.
- Use `rg` locally for speed and better ignore-file behavior.

## Version and release line
- Local check: `rg --version`
- Upstream release snapshot: ripgrep `15.1.0`.

