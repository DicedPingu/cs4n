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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `ssh username@remote_host` | Connect to a remote server |
| `ssh -i path/to/key_file username@remote_host` | Connect to a remote server with a specific [i]dentity (private key) |
| `ssh username@10.0.0.1 -p 2222` | Connect to a remote server with IP `10.0.0.1` and using a specific [p]ort (Note: `10.0.0.1` can be shortened to `10.1`) |
| `ssh username@remote_host -t command command_arguments` | Run a command on a remote server with a [t]ty allocation allowing interaction with the remote command |
| `ssh -D 1080 username@remote_host` | SSH tunneling: [D]ynamic port forwarding (SOCKS proxy on `localhost:1080`) |
| `ssh -L 9999:example.org:80 -N -T username@remote_host` | SSH tunneling: Forward a specific port (`localhost:9999` to `example.org:80`) along with disabling pseudo-[T]ty allocation and executio[N] of remote commands |
| `ssh -J username@jump_host username@remote_host` | SSH [J]umping: Connect through a jumphost to a remote server (Multiple jump hops may be specified separated by comma characters) |
| `<Enter><~><.>` | Close a hanged session |
| `ssh --help` | Show command usage and option reference |
| `man ssh` | Open the full manual page |
| `whatis ssh` | Print one-line command description |
| `type -a ssh` | Show how the shell resolves the command path |
| `command -v ssh` | Print executable path used by current shell |
| `tldr ssh` | Show concise command examples |
| `apropos ssh` | Search manual database for related commands |
| `ssh --version` | Print local tool version |
