# `apt-config` cheat sheet
APT Configuration Query program.

## Syntax
- Primary usage: `sudo apt-config [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-config dump` | Print the full active APT configuration tree |
| `apt-config shell APT_ARCH APT::Architecture` | Read a config key into a shell variable |
| `apt-config shell CACHE_DIR Dir::Cache` | Inspect configured cache directory quickly |
| `apt-config dump \| rg Acquire::` | Review downloader and network options |
| `apt-config dump \| rg -n Dir::` | Inspect configured filesystem paths for APT state/cache |
| `apt-config shell LISTS_DIR Dir::State::lists` | Print where package list files are stored |
| `apt-config --help` | Show command usage and option reference |
| `man apt-config` | Open the full manual page |
| `whatis apt-config` | Print one-line command description |
| `type -a apt-config` | Show how the shell resolves the command path |
| `command -v apt-config` | Print executable path used by current shell |
| `tldr apt-config` | Show concise command examples |
| `apropos apt-config` | Search manual database for related commands |
| `apt-config --version` | Print local tool version |
