# systemctl - control systemd services and units
Use it to manage service lifecycle, startup behavior, and unit state.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily service control
- `systemctl status <service>` - current state and recent logs.
- `sudo systemctl start <service>` - start now.
- `sudo systemctl stop <service>` - stop now.
- `sudo systemctl restart <service>` - restart after config/app changes.

## Boot and enablement
- `sudo systemctl enable <service>` - start on boot.
- `sudo systemctl disable <service>` - disable boot start.
- `systemctl is-active <service>` - machine-friendly active check.
- `systemctl is-enabled <service>` - machine-friendly boot check.

## Unit file changes
- `sudo systemctl daemon-reload` - reload unit definitions after edits.
- `sudo systemctl edit <service>` - create override drop-in.
- `systemctl cat <service>` - show full unit plus overrides.

## Cross-check with logs
- `journalctl -u <service> -n 100 --no-pager` - immediate diagnostics after restart.

## Version and release line
- Local check: `systemctl --version`
- Upstream release snapshot: systemd `259.1`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `systemctl status` | Show all running services |
| `systemctl --failed` | List failed units |
| `systemctl start\|stop\|restart\|reload\|status unit` | Start/Stop/Restart/Reload/Show the status of a service |
| `systemctl enable\|disable unit` | Enable/Disable a unit to be started on bootup |
| `systemctl daemon-reload` | Reload systemd, scan for new or changed units |
| `systemctl is-active\|is-enabled\|is-failed unit` | Check if a unit is active/enabled/failed |
| `systemctl list-units [-t\|--type] service\|socket\|automount --state failed\|running` | List all service/socket/automount units filtering by running/failed state |
| `systemctl cat\|edit unit` | Show the contents & absolute path of a unit file or edit it |
| `systemctl --help` | Show command usage and option reference |
| `man systemctl` | Open the full manual page |
| `whatis systemctl` | Print one-line command description |
| `type -a systemctl` | Show how the shell resolves the command path |
| `command -v systemctl` | Print executable path used by current shell |
| `tldr systemctl` | Show concise command examples |
| `apropos systemctl` | Search manual database for related commands |
| `systemctl --version` | Print local tool version |
