# `apt-show-versions` cheat sheet
Lists available package versions with distribution.

## Syntax
- Primary usage: `sudo apt-show-versions [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-show-versions` | List package versions and upgrade state |
| `apt-show-versions -u` | Show only packages that can be upgraded |
| `apt-show-versions <package>` | Show version state for a specific package |
| `apt-show-versions -a <package>` | Show all known versions for a package |
| `apt-show-versions -b` | Show upgrade blockers/broken package states |
| `apt-show-versions -r` | Report package states using repository data |
| `apt-show-versions --help` | Show command usage and option reference |
| `man apt-show-versions` | Open the full manual page |
| `whatis apt-show-versions` | Print one-line command description |
| `type -a apt-show-versions` | Show how the shell resolves the command path |
| `command -v apt-show-versions` | Print executable path used by current shell |
| `tldr apt-show-versions` | Show concise command examples |
| `apropos apt-show-versions` | Search manual database for related commands |
| `apt-show-versions --version` | Print local tool version |
