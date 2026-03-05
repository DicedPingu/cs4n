# `apt-show-source` cheat sheet
Lists source-packages.

## Syntax
- Primary usage: `sudo apt-show-source [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-show-source <package>` | Show source package info for a binary package |
| `apt-show-source --all <package>` | Display all source records related to a package |
| `apt-show-source --package-only <package>` | Limit output to package names |
| `apt-show-source --verbose <package>` | Print detailed source metadata |
| `apt-show-source --help` | Show apt-show-source options and filters |
| `apt-show-source <package> \| less` | Inspect complete source metadata output |
| `man apt-show-source` | Open the full manual page |
| `whatis apt-show-source` | Print one-line command description |
| `type -a apt-show-source` | Show how the shell resolves the command path |
| `command -v apt-show-source` | Print executable path used by current shell |
| `tldr apt-show-source` | Show concise command examples |
| `apropos apt-show-source` | Search manual database for related commands |
| `apt-show-source --version` | Print local tool version |
