# mkdir - create directories
# Use it to make project and data directories safely in scripts and shells.

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

