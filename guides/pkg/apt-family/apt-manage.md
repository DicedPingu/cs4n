# `apt-manage` cheat sheet
APT ecosystem utility command.

## Syntax
- Primary usage: `sudo apt-manage [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-manage --help` | Show apt-manage subcommands and options |
| `apt-manage list` | List configured software sources through apt-manage |
| `apt-manage mirror list` | Inspect known mirror presets or configurations |
| `apt-manage mirror select` | Interactively choose mirrors if supported by the tool version |
| `apt-manage source list` | Display source entries managed by apt-manage |
| `apt-manage update` | Refresh metadata after source or mirror changes |
| `man apt-manage` | Open the full manual page |
| `whatis apt-manage` | Print one-line command description |
| `type -a apt-manage` | Show how the shell resolves the command path |
| `command -v apt-manage` | Print executable path used by current shell |
| `tldr apt-manage` | Show concise command examples |
| `apropos apt-manage` | Search manual database for related commands |
| `apt-manage --version` | Print local tool version |
