# journalctl — systemd logs
# Use it to read and filter system logs.

- `journalctl -u <service>` — logs for a service
- `journalctl -f` — follow logs
- `journalctl -xe` — recent errors with context
- `journalctl --since "1 hour ago"` — time range
- `journalctl -b` — current boot
- `journalctl -b -1` — previous boot
