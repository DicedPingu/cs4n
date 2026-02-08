# rsync - incremental file synchronization
# Use it for fast local or remote copies, backups, and mirrors.

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

