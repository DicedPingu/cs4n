# systemctl Quicksheet
Manage systemd services.

## service basics
- `systemctl status ssh`
  - What it does: Shows current service status.
  - When to use it: Quick health check.
- `systemctl start ssh`
  - What it does: Starts a service.
  - When to use it: Manual start after config change.
- `systemctl stop ssh`
  - What it does: Stops a service.
  - When to use it: Maintenance or troubleshooting.
- `systemctl restart ssh`
  - What it does: Restarts a service.
  - When to use it: Apply config changes.

## enable on boot
- `systemctl enable ssh`
  - What it does: Enables service at boot.
  - When to use it: Keep service running after reboot.
- `systemctl disable ssh`
  - What it does: Disables service at boot.
  - When to use it: Prevent auto-start.

## inspection
- `systemctl list-units --type=service --state=running`
  - What it does: Lists running services.
  - When to use it: See what’s active.
- `systemctl cat ssh`
  - What it does: Shows the unit file.
  - When to use it: Inspect service definition.

## system targets
- `systemctl get-default`
  - What it does: Shows default boot target.
  - When to use it: Boot mode checks.
- `systemctl set-default multi-user.target`
  - What it does: Sets default boot target.
  - When to use it: Switch between GUI and CLI boots.
