# Linux Command Guides
Daily Linux command cheats grouped by file, text processing, networking, and system control.

## Files and locations
- Basics: `ls.md`, `cat.md`, `mkdir.md`, `mv.md`, `touch.md`
- Search/transform: `find.md`, `grep.md`, `sed.md`, `awk.md`, `xargs.md`
- System/network: `systemctl.md`, `journalctl.md`, `ssh.md`, `curl.md`, `htop.md`, `fwupd.md`
- Packaging/backup: `tar.md`, `rsync.md`
- Other essentials: `chmod_chown.md`, `head_tail.md`

## Recommended order
1. File basics
2. Search/transform tools
3. Service and log operations
4. Archive/transfer commands

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `ls -lah` | Show full directory listing with hidden files |
| `find . -maxdepth 3 -type f -name '*.md'` | Find markdown files within 3 levels |
| `grep -RIn '<pattern>' .` | Recursive search with line numbers |
| `sed -n '1,120p' <file>` | Print a selected line range |
| `awk '{print $1}' <file>` | Print first field from each line |
| `xargs -0 -I{} echo {}` | Safe null-delimited argument expansion |
| `journalctl -u <service> -n 100 --no-pager` | View latest logs for one service |
| `systemctl status <service>` | Check service state quickly |
| `ssh -o StrictHostKeyChecking=accept-new <user>@<host>` | Safer first-time host key accept |
| `curl -fsS '<url>'` | Fetch URL with failure visibility |
| `tar -czf backup.tgz <path>` | Compress a directory tree |
| `rsync -avh --progress <src>/ <dst>/` | Copy/sync with metadata and progress |
