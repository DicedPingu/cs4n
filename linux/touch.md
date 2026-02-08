# touch - create empty files or change timestamps
# Use it to initialize files and manipulate mtime/atime in scripts.

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

