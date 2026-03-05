# sed - stream editor for text transforms
Use it for line filtering and in-place replacements.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Fast patterns
- `sed -n '1,20p' file` - print line range.
- `sed 's/old/new/' file` - replace first match per line.
- `sed 's/old/new/g' file` - replace all matches per line.
- `sed '/^#/d' file` - drop comment lines.

## In-place edits (careful)
- `sed -i 's/old/new/g' file` - edit file directly.
- `sed -i.bak 's/old/new/g' file` - keep backup copy.

## Multi-step transforms
- `sed -e 's/foo/bar/g' -e '/^$/d' file` - chain expressions.
- `rg -l 'old' . | xargs sed -i 's/old/new/g'` - repo-wide replacement (review first).

## Version and release line
- Local check: `sed --version`
- Upstream release snapshot: GNU sed `4.9`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `command \| sed 's/apple/mango/g'` | Replace all `apple` (basic `regex`) occurrences with `mango` (basic `regex`) in all input lines and print the result to `stdout` |
| `command \| sed -f path/to/script.sed` | Execute a specific script [f]ile and print the result to `stdout` |
| `command \| sed -n '1p'` | Print just a first line to `stdout` |
| `sed --help` | Show command usage and option reference |
| `man sed` | Open the full manual page |
| `whatis sed` | Print one-line command description |
| `type -a sed` | Show how the shell resolves the command path |
| `command -v sed` | Print executable path used by current shell |
| `tldr sed` | Show concise command examples |
| `apropos sed` | Search manual database for related commands |
| `sed --version` | Print local tool version |
