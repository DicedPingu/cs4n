# mkdir - create directories
Use it to make project and data directories safely in scripts and shells.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Most common patterns
- `mkdir project` - create one directory.
- `mkdir -p a/b/c` - create parent chain if missing.
- `mkdir -m 755 shared` - create with explicit permissions.

## Script-safe usage
- `mkdir -p "$TARGET_DIR"` - idempotent directory creation.
- `install -d -m 750 /path/to/dir` - create directory with ownership/perm control in install scripts.

## Version and release line
- Local check: `mkdir --version`
- Upstream release snapshot: GNU coreutils `9.10`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `mkdir path/to/directory1 path/to/directory2 ...` | Create specific directories |
| `mkdir [-p\|--parents] path/to/directory1 path/to/directory2 ...` | Create specific directories and their parents if needed |
| `mkdir [-m\|--mode] rwxrw-r-- path/to/directory1 path/to/directory2 ...` | Create directories with specific permissions |
| `mkdir [-p\|--parents] path/to/{a,b}/{x,y,z}/{h,i,j}` | Create multiple nested directories recursively |
| `mkdir --help` | Show command usage and option reference |
| `man mkdir` | Open the full manual page |
| `whatis mkdir` | Print one-line command description |
| `type -a mkdir` | Show how the shell resolves the command path |
| `command -v mkdir` | Print executable path used by current shell |
| `tldr mkdir` | Show concise command examples |
| `apropos mkdir` | Search manual database for related commands |
| `mkdir --version` | Print local tool version |
