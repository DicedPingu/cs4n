# grep - pattern search in text
Use it for fast filtering in files, logs, and pipelines.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Core usage
- `grep "term" file` - basic search.
- `grep -n "term" file` - include line numbers.
- `grep -i "term" file` - case-insensitive search.
- `grep -r "term" .` - recursive directory search.

## Better matching control
- `grep -E "warn|error" file` - extended regex.
- `grep -F "literal.text" file` - fixed-string mode.
- `grep -v "term" file` - invert match.
- `grep -C 2 "term" file` - show surrounding context.

## Typical pairings
- `journalctl -u app | grep -i error` - service error stream.
- `ps aux | grep '[n]ginx'` - avoid matching the grep process line.

## Version and release line
- Local check: `grep --version`
- Upstream release snapshot: GNU grep `3.12`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `grep "search_pattern" path/to/file1 path/to/file2 ...` | Search for a pattern within a file |
| `grep [-F\|--fixed-strings] "exact_string" path/to/file` | Search for an exact string (disables `regex`es) |
| `grep [-rnI\|--recursive --line-number --binary-files=without-match] "search_pattern" path/to/directory` | Search for a pattern in all files recursively in a directory, showing line numbers of matches, ignoring binary files |
| `grep [-Ei\|--extended-regexp --ignore-case] "search_pattern" path/to/file` | Use extended `regex`es (supports `?`, `+`, `{}`, `()`, and `\|`), in case-insensitive mode |
| `grep --context\|--before-context\|--after-context 3 "search_pattern" path/to/file` | Print 3 lines of [C]ontext around, [B]efore or [A]fter each match |
| `grep [-Hn\|--with-filename --line-number] --color=always "search_pattern" path/to/file` | Print file name and line number for each match with color output |
| `grep [-o\|--only-matching] "search_pattern" path/to/file` | Search for lines matching a pattern, printing only the matched text |
| `cat path/to/file \| grep [-v\|--invert-match] "search_pattern"` | Search `stdin` for lines that do not match a pattern |
| `grep --help` | Show command usage and option reference |
| `man grep` | Open the full manual page |
| `whatis grep` | Print one-line command description |
| `type -a grep` | Show how the shell resolves the command path |
| `command -v grep` | Print executable path used by current shell |
| `tldr grep` | Show concise command examples |
| `apropos grep` | Search manual database for related commands |
| `grep --version` | Print local tool version |
