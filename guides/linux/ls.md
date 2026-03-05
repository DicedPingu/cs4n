# ls - list directory contents
Use it to inspect files quickly with the amount of detail you need.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily listing patterns
- `ls` - names only.
- `ls -la` - include hidden files and metadata.
- `ls -lh` - human-readable sizes.
- `ls -lt` - newest first.

## Useful sort and format flags
- `ls -lS` - sort by size.
- `ls -ltr` - oldest first.
- `ls -d */` - list directories only.
- `ls --group-directories-first` - cleaner mixed listings.

## Better tools for deep trees
- `find . -maxdepth 2 -type f` - recursive and scriptable.
- `tree -a -L 2` - visual hierarchy (if installed).

## Version and release line
- Local check: `ls --version`
- Upstream release snapshot: GNU coreutils `9.10`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `ls -1` | List files one per line |
| `ls [-a\|--all]` | List all files, including hidden files |
| `ls [-F\|--classify]` | List files with a trailing symbol to indicate file type (directory/, symbolic_link@, executable*, ...) |
| `ls [-la\|-l --all]` | List all files in [l]ong format (permissions, ownership, size, and modification date) |
| `ls [-lh\|-l --human-readable]` | List files in [l]ong format with size displayed using human-readable units (KiB, MiB, GiB) |
| `ls [-lSR\|-lS --recursive]` | List files in [l]ong format, sorted by [S]ize (descending) recursively |
| `ls [-ltr\|-lt --reverse]` | List files in [l]ong format, sorted by [t]ime the file was modified and in reverse order (oldest first) |
| `ls [-d\|--directory] */` | Only list directories |
| `ls --help` | Show command usage and option reference |
| `man ls` | Open the full manual page |
| `whatis ls` | Print one-line command description |
| `type -a ls` | Show how the shell resolves the command path |
| `command -v ls` | Print executable path used by current shell |
| `tldr ls` | Show concise command examples |
| `apropos ls` | Search manual database for related commands |
| `ls --version` | Print local tool version |
