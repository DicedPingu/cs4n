# find - recursive file search and action runner
Use it to locate files by name/type/time and perform batch actions safely.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## High-value searches
- `find . -type f -name "*.log"` - find log files.
- `find . -type d -name "node_modules"` - find directories.
- `find . -mtime -1` - modified in last 24 hours.
- `find . -maxdepth 2 -name "*.md"` - limit recursion depth.

## Safer batch actions
- `find . -name "*.tmp" -print` - inspect first.
- `find . -name "*.tmp" -delete` - delete matches after confirming.
- `find . -type f -name "*.py" -exec rg -n "TODO" {} +` - pass many files per exec.

## Space-safe piping
- `find . -type f -print0 | xargs -0 rm` - robust with spaces/newlines.
- `find . -type f -print0 | xargs -0 -n1 basename` - transform file list safely.

## Version and release line
- Local check: `find --version`
- Upstream release snapshot: GNU findutils `4.10.0`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `find root_path -name '*.ext'` | Find files by extension |
| `find root_path -path '*/path/*/*.ext' -or -name '*pattern*'` | Find files matching multiple path/name patterns |
| `find root_path -type d -iname '*lib*'` | Find directories matching a given name, in case-insensitive mode |
| `find root_path -name '*.py' -not -path '*/site-packages/*'` | Find files matching a given pattern, excluding specific paths |
| `find root_path -maxdepth 1 -size +500k -size -10M` | Find files matching a given size range, limiting the recursive depth to "1" |
| `find root_path -name '*.ext' -exec wc -l {} \;` | Run a command for each file (use `{}` within the command to access the filename) |
| `find root_path -daystart -mtime -1 -exec tar -cvf archive.tar {} \+` | Find all files modified today and pass the results to a single command as arguments |
| `find root_path -type f\|d -empty -delete -print` | Search for either empty files or directories and delete them verbosely |
| `find --help` | Show command usage and option reference |
| `man find` | Open the full manual page |
| `whatis find` | Print one-line command description |
| `type -a find` | Show how the shell resolves the command path |
| `command -v find` | Print executable path used by current shell |
| `tldr find` | Show concise command examples |
| `apropos find` | Search manual database for related commands |
| `find --version` | Print local tool version |
