# htop - interactive process viewer
Use it for CPU/RAM inspection and process management from a live TUI.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Typical session
- `htop` - open interactive dashboard.
- `htop -u <user>` - focus one user's processes.
- `htop -p <pid1,pid2>` - inspect selected process IDs.

## High-value keys
- `F3` - search process list.
- `F4` - filter process list.
- `F5` - tree view.
- `F6` - change sort column.
- `F9` - send signal/kill.

## Fast alternatives
- `top` - available almost everywhere (lower overhead).
- `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu | head` - scriptable snapshot.

## Version and release line
- Local check: `htop --version`
- Upstream release snapshot: htop `3.4.1`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `htop` | Start `htop` |
| `htop [-u\|--user] username` | Start `htop` displaying processes owned by a specific user |
| `htop [-t\|--tree]` | Display processes hierarchically in a tree view to show the parent-child relationships |
| `htop [-s\|--sort] sort_item` | Sort processes by a specified `sort_item` (use `htop --sort help` for available options) |
| `htop [-d\|--delay] 50` | Start `htop` with the specified delay between updates, in tenths of a second (i.e. 50 = 5 seconds) |
| `htop --readonly` | Disable all system and process changing features |
| `<F1>\|<?>` | See interactive commands while running `htop` |
| `<Tab>` | Switch to a different tab |
| `htop --help` | Show command usage and option reference |
| `man htop` | Open the full manual page |
| `whatis htop` | Print one-line command description |
| `type -a htop` | Show how the shell resolves the command path |
| `command -v htop` | Print executable path used by current shell |
| `tldr htop` | Show concise command examples |
| `apropos htop` | Search manual database for related commands |
| `htop --version` | Print local tool version |
