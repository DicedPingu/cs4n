# mv - move or rename files
Use it to rename paths and relocate files/directories.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Common operations
- `mv old new` - rename file or directory.
- `mv file dir/` - move into target directory.
- `mv *.log archive/` - bulk move by glob.

## Safer overwrite behavior
- `mv -i src dest` - prompt before overwrite.
- `mv -n src dest` - do not overwrite existing file.
- `mv -v src dest` - verbose moves for logs/scripts.

## Related commands
- `cp -a src dest && rm -rf src` - cross-device fallback when move semantics are blocked.
- `rsync -av --remove-source-files src/ dest/` - controlled large transfers.

## Version and release line
- Local check: `mv --version`
- Upstream release snapshot: GNU coreutils `9.10`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `mv path/to/source path/to/target` | Rename a file or directory when the target is not an existing directory |
| `mv path/to/source path/to/existing_directory` | Move a file or directory into an existing directory |
| `mv path/to/source1 path/to/source2 ... path/to/existing_directory` | Move multiple files into an existing directory, keeping the filenames unchanged |
| `mv [-f\|--force] path/to/source path/to/target` | Do not prompt for confirmation before overwriting existing files |
| `mv [-i\|--interactive] path/to/source path/to/target` | Prompt for confirmation interactively before overwriting existing files, regardless of file permissions |
| `mv [-n\|--no-clobber] path/to/source path/to/target` | Do not overwrite existing files at the target |
| `mv [-v\|--verbose] path/to/source path/to/target` | Move files in verbose mode, showing files after they are moved |
| `find /var/log -type f -name '*.log' -print0 \| xargs -0 mv [-t\|--target-directory] path/to/target_directory` | Specify target directory so that you can use external tools to gather movable files |
| `mv --help` | Show command usage and option reference |
| `man mv` | Open the full manual page |
| `whatis mv` | Print one-line command description |
| `type -a mv` | Show how the shell resolves the command path |
| `command -v mv` | Print executable path used by current shell |
| `tldr mv` | Show concise command examples |
| `apropos mv` | Search manual database for related commands |
| `mv --version` | Print local tool version |
