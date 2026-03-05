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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `journalctl [-b\|--boot] [-p\|--priority] 3` | Show all messages with priority level 3 (errors) from this boot |
| `journalctl --vacuum-time 2d` | Delete journal logs which are older than 2 days |
| `journalctl [-n\|--lines] n [-f\|--follow]` | Show only the last `n` lines and follow new messages (like `tail -f` for traditional syslog) |
| `journalctl [-u\|--unit] unit` | Show all messages by a specific unit |
| `journalctl _SYSTEMD_INVOCATION_ID=$(systemctl show --value --property=InvocationID unit)` | Show logs for a given unit since the last time it started |
| `journalctl [-S\|--since] now\|today\|yesterday\|tomorrow [-U\|--until] "YYYY-MM-DD HH:MM:SS"` | Filter messages within a time range (either timestamp or placeholders like "yesterday") |
| `journalctl _PID=pid` | Show all messages by a specific process |
| `journalctl path/to/executable` | Show all messages by a specific executable |
| `journalctl --help` | Show command usage and option reference |
| `man journalctl` | Open the full manual page |
| `whatis journalctl` | Print one-line command description |
| `type -a journalctl` | Show how the shell resolves the command path |
| `command -v journalctl` | Print executable path used by current shell |
| `tldr journalctl` | Show concise command examples |
| `apropos journalctl` | Search manual database for related commands |
| `journalctl --version` | Print local tool version |
