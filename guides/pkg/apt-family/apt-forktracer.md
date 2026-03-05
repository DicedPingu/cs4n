# `apt-forktracer` cheat sheet
a utility for managing package versions.

## Syntax
- Primary usage: `sudo apt-forktracer [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-forktracer` | Detect locally modified packages that diverge from repository versions |
| `apt-forktracer --sources` | Inspect package forks with source package mapping |
| `apt-forktracer --all` | Show all locally forked package candidates |
| `apt-forktracer --verbose` | Print additional diagnostic information |
| `apt-forktracer --help` | Show options and output format |
| `apt-forktracer \| less` | Review potentially forked packages page by page |
| `man apt-forktracer` | Open the full manual page |
| `whatis apt-forktracer` | Print one-line command description |
| `type -a apt-forktracer` | Show how the shell resolves the command path |
| `command -v apt-forktracer` | Print executable path used by current shell |
| `tldr apt-forktracer` | Show concise command examples |
| `apropos apt-forktracer` | Search manual database for related commands |
| `apt-forktracer --version` | Print local tool version |
