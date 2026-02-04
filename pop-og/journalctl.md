# journalctl Quicksheet
Query systemd logs.

## basics
- `journalctl`
  - What it does: Shows all logs (oldest to newest).
  - When to use it: Full system log browsing.
- `journalctl -xe`
  - What it does: Shows recent logs with explanations.
  - When to use it: Debugging failures.
- `journalctl -b`
  - What it does: Shows logs from the current boot.
  - When to use it: Boot-specific troubleshooting.

## service logs
- `journalctl -u ssh`
  - What it does: Shows logs for a service.
  - When to use it: Service-specific debugging.
- `journalctl -u ssh -b -n 100`
  - What it does: Last 100 lines for a service in this boot.
  - When to use it: Fast recent checks.

## time filtering
- `journalctl --since "1 hour ago"`
  - What it does: Shows logs since a time.
  - When to use it: Narrowing down incidents.
- `journalctl --since "2025-01-01" --until "2025-01-31"`
  - What it does: Logs in a date range.
  - When to use it: Audits and reviews.

## live tail
- `journalctl -f`
  - What it does: Follows logs live.
  - When to use it: Watching activity in real time.
