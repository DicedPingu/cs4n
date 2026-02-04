# rsync — fast file sync
# Use it for backups and incremental copies.

- `rsync -av src/ dest/` — archive copy
- `rsync -av --delete src/ dest/` — mirror exactly
- `rsync -avz src/ user@host:/path/` — sync over SSH
- `rsync -n -av src/ dest/` — dry run
