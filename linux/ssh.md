# ssh - secure remote shell and tunneling
# Use it for remote administration, secure file transfer, and port forwarding.

## Core connection patterns
- `ssh user@host` - connect with default key/agent.
- `ssh -p 2222 user@host` - custom SSH port.
- `ssh -i ~/.ssh/id_ed25519 user@host` - explicit private key.

## Key management and copy
- `ssh-keygen -t ed25519 -C "you@example.com"` - generate modern key pair.
- `ssh-copy-id user@host` - install public key on remote host.
- `scp file user@host:/path/` - copy file over SSH.

## Tunnels you will actually use
- `ssh -L 8080:localhost:8080 user@host` - local port forward.
- `ssh -N -f -L 5432:db.internal:5432 user@host` - background tunnel without shell.
- `ssh -J bastion user@target` - jump host flow.

## Useful config
- Add hosts to `~/.ssh/config` to reduce repeated flags.
- Use `ServerAliveInterval 30` for flaky networks.

## Version and release line
- Local check: `ssh -V`
- Upstream release snapshot: OpenSSH `9.9p2`.

