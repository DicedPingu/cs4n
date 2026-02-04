# systemctl — manage systemd services
# Use it to start/stop/inspect services.

- `systemctl status <svc>` — status + logs
- `systemctl start <svc>` — start
- `systemctl stop <svc>` — stop
- `systemctl restart <svc>` — restart
- `systemctl enable <svc>` — start on boot
- `systemctl disable <svc>` — disable on boot
- `systemctl is-active <svc>` — active?
- `systemctl daemon-reload` — reload unit files
