# touch - create empty files or change timestamps
Use it to initialize files and manipulate mtime/atime in scripts.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Common usage
- `touch file` - create file if missing, otherwise update timestamp.
- `touch -c file` - update only if file exists.
- `touch file1 file2 file3` - batch update.

## Timestamp control
- `touch -t 202602081230 file` - set explicit timestamp (`YYYYMMDDhhmm`).
- `touch -r reference.file target.file` - copy timestamp from another file.

## Version and release line
- Local check: `touch --version`
- Upstream release snapshot: GNU coreutils `9.10`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `touch path/to/file1 path/to/file2 ...` | Create specific files |
| `touch [-c\|--no-create] -a\|m path/to/file1 path/to/file2 ...` | Set the file [a]ccess or [m]odification times to the current one and don't create file if it doesn't exist |
| `touch [-c\|--no-create] -t YYYYMMDDHHMM.SS path/to/file1 path/to/file2 ...` | Set the file [t]ime to a specific value and don't create file if it doesn't exist |
| `touch [-c\|--no-create] [-r\|--reference] path/to/reference_file path/to/file1 path/to/file2 ...` | Set the files' timestamp to the reference file's timestamp, and do not create the file if it does not exist |
| `touch [-d\|--date] "last year\|5 hours\|next thursday\|nov 14\|..." path/to/file` | Set the timestamp by parsing a string |
| `touch path/to/file{1..10}` | Create multiple files with an increasing number |
| `touch path/to/file{a..z}` | Create multiple files with a letter range |
| `touch --help` | Show command usage and option reference |
| `man touch` | Open the full manual page |
| `whatis touch` | Print one-line command description |
| `type -a touch` | Show how the shell resolves the command path |
| `command -v touch` | Print executable path used by current shell |
| `tldr touch` | Show concise command examples |
| `apropos touch` | Search manual database for related commands |
| `touch --version` | Print local tool version |
