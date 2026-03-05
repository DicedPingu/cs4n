# `apt-get` cheat sheet
APT package handling utility -- command-line interface.

## Syntax
- Primary usage: `sudo apt-get [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt-get update` | Update the list of available packages and versions (it's recommended to run this before other `apt-get` commands) |
| `sudo apt-get install package` | Install a package, or update it to the latest available version |
| `sudo apt-get remove package` | Remove a package |
| `sudo apt-get purge package` | Remove a package and its configuration files |
| `sudo apt-get upgrade` | Upgrade all installed packages to their newest available versions |
| `apt-get autoclean` | Clean the local repository - removing package files (`.deb`) from interrupted downloads that can no longer be downloaded |
| `sudo apt-get autoremove` | Remove all packages that are no longer needed |
| `sudo apt-get dist-upgrade` | Upgrade installed packages (like `upgrade`), but remove obsolete packages and install additional packages to meet new dependencies |
| `apt-get --help` | Show command usage and option reference |
| `man apt-get` | Open the full manual page |
| `whatis apt-get` | Print one-line command description |
| `type -a apt-get` | Show how the shell resolves the command path |
| `command -v apt-get` | Print executable path used by current shell |
| `tldr apt-get` | Show concise command examples |
| `apropos apt-get` | Search manual database for related commands |
| `apt-get --version` | Print local tool version |
