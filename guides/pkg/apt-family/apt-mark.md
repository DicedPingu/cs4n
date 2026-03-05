# `apt-mark` cheat sheet
show, set and unset various settings for a package.

## Syntax
- Primary usage: `sudo apt-mark [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt-mark auto package` | Mark a package as automatically installed |
| `sudo apt-mark hold package` | Hold a package at its current version and prevent updates to it |
| `sudo apt-mark unhold package` | Allow a package to be updated again |
| `apt-mark showmanual` | Show manually installed packages |
| `apt-mark showhold` | Show held packages that aren't being updated |
| `apt-mark --help` | Show command usage and option reference |
| `man apt-mark` | Open the full manual page |
| `whatis apt-mark` | Print one-line command description |
| `type -a apt-mark` | Show how the shell resolves the command path |
| `command -v apt-mark` | Print executable path used by current shell |
| `tldr apt-mark` | Show concise command examples |
| `apropos apt-mark` | Search manual database for related commands |
| `apt-mark --version` | Print local tool version |
