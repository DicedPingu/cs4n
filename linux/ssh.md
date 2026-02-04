# ssh — secure remote shell
# Use it to connect to servers securely.

- `ssh user@host` — connect
- `ssh -p 2222 user@host` — custom port
- `ssh -i ~/.ssh/id_ed25519 user@host` — specific key
- `ssh -L 8080:localhost:8080 user@host` — local port forward
- `ssh -N -f -L 8080:localhost:8080 user@host` — background tunnel
- `ssh-copy-id user@host` — install SSH key
- `scp file user@host:/path/` — copy file
