# `apt-cache` cheat sheet
query the APT cache.

## Syntax
- Primary usage: `sudo apt-cache [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-cache search query` | Search for a package in your current sources |
| `apt-cache show package` | Show information about a package |
| `apt-cache policy package` | Show whether a package is installed and up to date |
| `apt-cache depends package` | Show dependencies for a package |
| `apt-cache rdepends package` | Show packages that depend on a particular package |
| `apt-cache --help` | Show command usage and option reference |
| `man apt-cache` | Open the full manual page |
| `whatis apt-cache` | Print one-line command description |
| `type -a apt-cache` | Show how the shell resolves the command path |
| `command -v apt-cache` | Print executable path used by current shell |
| `tldr apt-cache` | Show concise command examples |
| `apropos apt-cache` | Search manual database for related commands |
| `apt-cache --version` | Print local tool version |
