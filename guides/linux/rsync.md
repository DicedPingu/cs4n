# rsync - incremental file synchronization
Use it for fast local or remote copies, backups, and mirrors.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Primary workflows
- `rsync -av src/ dest/` - archive copy preserving metadata.
- `rsync -avz src/ user@host:/path/` - compressed remote sync over SSH.
- `rsync -av --delete src/ dest/` - make destination mirror source.

## Safety-first execution
- `rsync -anv src/ dest/` - dry run first.
- `rsync -av --progress src/ dest/` - transfer progress.
- `rsync -av --exclude '.git/' src/ dest/` - exclude patterns.

## Performance and reliability options
- `rsync -av --partial --inplace src/ dest/` - resume-friendly behavior for large files.
- `rsync -e "ssh -p 2222" -av src/ user@host:/path/` - custom SSH transport.

## Version and release line
- Local check: `rsync --version`
- Upstream release snapshot: rsync `3.4.1`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `rsync path/to/source path/to/destination` | Transfer a file |
| `rsync [-a\|--archive] path/to/source path/to/destination` | Use archive mode (recursively copy directories, copy symlinks without resolving, and preserve permissions, ownership and modification times) |
| `rsync [-zvhP\|--compress --verbose --human-readable --partial --progress] path/to/source path/to/destination` | Compress the data as it is sent to the destination, display verbose and human-readable progress, and keep partially transferred files if interrupted |
| `rsync [-r\|--recursive] path/to/source path/to/destination` | Recursively copy directories |
| `rsync [-r\|--recursive] path/to/source/ path/to/destination` | Transfer directory contents, but not the directory itself |
| `rsync [-auL\|--archive --update --copy-links] path/to/source path/to/destination` | Use archive mode, resolve symlinks, and skip files that are newer on the destination |
| `rsync [-r\|--recursive] --delete rsync://host:path/to/source path/to/destination` | Transfer a directory from a remote host running `rsyncd` and delete files on the destination that do not exist on the source |
| `rsync [-e\|--rsh] 'ssh -p port' --info=progress2 host:path/to/source path/to/destination` | Transfer a file over SSH using a different port than the default (22) and show global progress |
| `rsync --help` | Show command usage and option reference |
| `man rsync` | Open the full manual page |
| `whatis rsync` | Print one-line command description |
| `type -a rsync` | Show how the shell resolves the command path |
| `command -v rsync` | Print executable path used by current shell |
| `tldr rsync` | Show concise command examples |
| `apropos rsync` | Search manual database for related commands |
| `rsync --version` | Print local tool version |
