# `apt-move` cheat sheet
move cache of Debian packages into a mirror hierarchy.

## Syntax
- Primary usage: `sudo apt-move [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt-move update` | Move downloaded packages into archive structure and update indices |
| `sudo apt-move delete` | Delete obsolete package files from move-managed archive |
| `sudo apt-move local` | Process local package caches according to apt-move config |
| `sudo apt-move move` | Perform package moving operations without full update cycle |
| `apt-move -f /etc/apt-move.conf update` | Use an explicit apt-move config path |
| `apt-move --help` | Show apt-move modes and options |
| `man apt-move` | Open the full manual page |
| `whatis apt-move` | Print one-line command description |
| `type -a apt-move` | Show how the shell resolves the command path |
| `command -v apt-move` | Print executable path used by current shell |
| `tldr apt-move` | Show concise command examples |
| `apropos apt-move` | Search manual database for related commands |
| `apt-move --version` | Print local tool version |
