# `apt-key` cheat sheet
APT ecosystem utility command.

## Syntax
- Primary usage: `sudo apt-key [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-key list` | List trusted keys |
| `apt-key add public_key_file.asc` | Add a key to the trusted keystore |
| `apt-key del key_id` | Delete a key from the trusted keystore |
| `wget [-qO\|--quiet --output-document] - https://host.tld/filename.key \| apt-key add -` | Add a remote key to the trusted keystore |
| `apt-key adv --keyserver pgp.mit.edu --recv KEYID` | Add a key from keyserver with only key ID |
| `sudo apt-key list` | Legacy key list command (deprecated on modern systems) |
| `sudo apt-key del <keyid>` | Legacy key removal command (deprecated) |
| `sudo install -d -m 0755 /etc/apt/keyrings` | Create keyring directory for modern signed-by workflow |
| `curl -fsSL <key-url> \| gpg --dearmor \| sudo tee /etc/apt/keyrings/<repo>.gpg >/dev/null` | Install repository key to dedicated keyring |
| `echo "deb [signed-by=/etc/apt/keyrings/<repo>.gpg] <repo-url> <suite> <components>" \| sudo tee /etc/apt/sources.list.d/<repo>.list` | Add source entry using keyring pinning |
| `sudo apt update` | Validate repository metadata after key migration |
| `apt-key --help` | Show command usage and option reference |
| `man apt-key` | Open the full manual page |
| `whatis apt-key` | Print one-line command description |
| `type -a apt-key` | Show how the shell resolves the command path |
| `command -v apt-key` | Print executable path used by current shell |
| `tldr apt-key` | Show concise command examples |
| `apropos apt-key` | Search manual database for related commands |
| `apt-key --version` | Print local tool version |

## Note
- `apt-key` is deprecated on modern Debian/Ubuntu releases. Prefer per-repo keyrings in `/etc/apt/keyrings` with `signed-by=` source entries.
