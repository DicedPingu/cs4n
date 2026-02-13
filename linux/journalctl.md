# journalctl - systemd journal query tool
Use it to inspect service logs by unit, boot, severity, and time window.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Most common filters
- `journalctl -u <service>` - logs for one unit.
- `journalctl -u <service> -f` - follow live service logs.
- `journalctl -b` - logs from current boot.
- `journalctl -b -1` - logs from previous boot.

## Time and severity slicing
- `journalctl --since "1 hour ago"` - recent history.
- `journalctl --since "2026-02-08 10:00" --until "2026-02-08 11:00"` - exact interval.
- `journalctl -p err..alert` - error and higher severity.
- `journalctl -xeu <service>` - errors with explanatory context.

## Export and machine-friendly output
- `journalctl -u <service> -n 200 > service.log` - export subset.
- `journalctl -u <service> -o short-iso` - stable timestamp format.
- `journalctl -u <service> -o json-pretty` - structured output.

## Version and release line
- Local check: `journalctl --version`
- Upstream release snapshot: systemd `259.1`.

