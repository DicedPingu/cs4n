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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `rg pattern` | Recursively search current directory for a pattern (`regex`) |
| `rg pattern path/to/file_or_directory` | Recursively search for a pattern in a file or directory |
| `rg [-.\|--hidden] --no-ignore pattern` | Include hidden files and entries listed in `.gitignore` |
| `rg pattern [-g\|--glob] filename_glob_pattern` | Only search the files whose names match the glob pattern(s) (e.g. `README.*`) |
| `rg --files \| rg pattern` | Recursively list filenames in the current directory that match a pattern |
| `rg [-l\|--files-with-matches] pattern` | Only list matched files (useful when piping to other commands) |
| `rg [-v\|--invert-match] pattern` | Show lines that do not match the pattern |
| `rg [-F\|--fixed-strings] -- string` | Search for a literal string pattern |
| `rg --help` | Show command usage and option reference |
| `man rg` | Open the full manual page |
| `whatis rg` | Print one-line command description |
| `type -a rg` | Show how the shell resolves the command path |
| `command -v rg` | Print executable path used by current shell |
| `tldr rg` | Show concise command examples |
| `apropos rg` | Search manual database for related commands |
| `rg --version` | Print local tool version |
