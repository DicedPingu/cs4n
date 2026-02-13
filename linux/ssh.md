# ssh - secure remote shell and tunneling
Use it for server access, GitHub auth keys, and secure connections across devices.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Core connection patterns
- `ssh user@host` - connect with default key/agent.
- `ssh -p 2222 user@host` - custom SSH port.
- `ssh -i ~/.ssh/id_ed25519 user@host` - explicit private key.

## Multi-device key setup (Pop!_OS + Android)
### Generate separate keys per device
- Pop!_OS: `ssh-keygen -t ed25519 -a 100 -f ~/.ssh/id_ed25519_popos -C "you@popos"`
- Android/Termux: `ssh-keygen -t ed25519 -a 100 -f ~/.ssh/id_ed25519_android -C "you@android"`

### Add keys to GitHub
- `gh ssh-key add ~/.ssh/id_ed25519_popos.pub --title "popos-main"`
- `gh ssh-key add ~/.ssh/id_ed25519_android.pub --title "android-termux"`
- `ssh -T git@github.com` - verify auth.

### Recommended `~/.ssh/config`
```sshconfig
Host github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_popos
  IdentitiesOnly yes
```

## Key management and copy
- `ssh-copy-id user@host` - install public key on remote host.
- `scp file user@host:/path/` - copy file over SSH.
- `sftp user@host` - interactive secure file transfer.

## Tunnels you will actually use
- `ssh -L 8080:localhost:8080 user@host` - local port forward.
- `ssh -N -f -L 5432:db.internal:5432 user@host` - background tunnel without shell.
- `ssh -J bastion user@target` - jump host flow.

## Security and reliability notes
- Never sync private keys via cloud drives or Git repos.
- Prefer one revocable key per device.
- Use `ServerAliveInterval 30` and `ServerAliveCountMax 3` for unstable links.

## Version and release line
- Local check: `ssh -V`
- Upstream release snapshot: OpenSSH `9.9p2`.
