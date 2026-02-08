# mv - move or rename files
# Use it to rename paths and relocate files/directories.

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

