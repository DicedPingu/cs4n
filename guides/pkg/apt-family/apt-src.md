# `apt-src` cheat sheet
manage debian source package trees.

## Syntax
- Primary usage: `sudo apt-src [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-src update` | Refresh source package metadata |
| `apt-src list` | List available source packages |
| `apt-src install <source-package>` | Download and unpack source package into working directory |
| `apt-src build <source-package>` | Build a package from source using apt-src workflow |
| `apt-src remove <source-package>` | Remove source package trees managed by apt-src |
| `apt-src --help` | Show apt-src commands and option syntax |
| `man apt-src` | Open the full manual page |
| `whatis apt-src` | Print one-line command description |
| `type -a apt-src` | Show how the shell resolves the command path |
| `command -v apt-src` | Print executable path used by current shell |
| `tldr apt-src` | Show concise command examples |
| `apropos apt-src` | Search manual database for related commands |
| `apt-src --version` | Print local tool version |
