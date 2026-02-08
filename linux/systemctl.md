# systemctl - control systemd services and units
# Use it to manage service lifecycle, startup behavior, and unit state.

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

