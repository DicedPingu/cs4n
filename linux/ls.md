# ls - list directory contents
# Use it to inspect files quickly with the amount of detail you need.

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

