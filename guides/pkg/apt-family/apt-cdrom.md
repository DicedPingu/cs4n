# `apt-cdrom` cheat sheet
APT CD-ROM management utility.

## Syntax
- Primary usage: `sudo apt-cdrom [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt-cdrom add` | Scan CD/DVD and add it as a package source |
| `sudo apt-cdrom ident` | Show ID information for an inserted disc |
| `sudo apt-cdrom -m add` | Add disc without trying to mount automatically |
| `sudo apt-cdrom -d /media/cdrom add` | Use a specific mount path for the disc |
| `sudo apt-cdrom -r add` | Rename source entries while adding media |
| `sudo apt-cdrom -o Debug::Acquire::cdrom=true add` | Troubleshoot media detection with debug output |
| `apt-cdrom --help` | Show command usage and option reference |
| `man apt-cdrom` | Open the full manual page |
| `whatis apt-cdrom` | Print one-line command description |
| `type -a apt-cdrom` | Show how the shell resolves the command path |
| `command -v apt-cdrom` | Print executable path used by current shell |
| `tldr apt-cdrom` | Show concise command examples |
| `apropos apt-cdrom` | Search manual database for related commands |
| `apt-cdrom --version` | Print local tool version |
