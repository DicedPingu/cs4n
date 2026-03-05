# `apt-cudf` cheat sheet
CUDF solver integration for APT.

## Syntax
- Primary usage: `sudo apt-cudf [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-cudf --help` | Show CUDF solver bridge usage and options |
| `apt-cudf-get --help` | Inspect apt-cudf-get options for solver-driven installs |
| `apt-cudf --solver aspcud --help` | Verify solver wiring before using advanced upgrades |
| `apt-cudf-get install <package>` | Install with CUDF solver backend if configured |
| `apt-cudf-get dist-upgrade` | Attempt a distribution upgrade via CUDF solver |
| `apt-cudf-get remove <package>` | Remove package while letting CUDF resolve transitions |
| `man apt-cudf` | Open the full manual page |
| `whatis apt-cudf` | Print one-line command description |
| `type -a apt-cudf` | Show how the shell resolves the command path |
| `command -v apt-cudf` | Print executable path used by current shell |
| `tldr apt-cudf` | Show concise command examples |
| `apropos apt-cudf` | Search manual database for related commands |
| `apt-cudf --version` | Print local tool version |
