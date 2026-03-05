# `apt-cudf-get` cheat sheet
wrapper for calling apt-get with external solvers.

## Syntax
- Primary usage: `sudo apt-cudf-get [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-cudf-get update` | Refresh package metadata for CUDF-driven actions |
| `apt-cudf-get install <package>` | Install package through CUDF resolver path |
| `apt-cudf-get remove <package>` | Remove package with CUDF solver decisions |
| `apt-cudf-get dist-upgrade` | Run a full upgrade with CUDF objective solving |
| `apt-cudf-get --solver aspcud install <package>` | Select a specific external CUDF solver |
| `apt-cudf-get --simulate install <package>` | Preview CUDF resolution without making changes |
| `apt-cudf-get --help` | Show command usage and option reference |
| `man apt-cudf-get` | Open the full manual page |
| `whatis apt-cudf-get` | Print one-line command description |
| `type -a apt-cudf-get` | Show how the shell resolves the command path |
| `command -v apt-cudf-get` | Print executable path used by current shell |
| `tldr apt-cudf-get` | Show concise command examples |
| `apropos apt-cudf-get` | Search manual database for related commands |
| `apt-cudf-get --version` | Print local tool version |
