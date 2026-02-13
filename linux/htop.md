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

