# `apt-file` cheat sheet
- APT package searching utility -- command-line interface.

## Syntax
- Primary usage: `sudo apt-file [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt update` | Update the metadata database |
| `apt-file search\|find path/to/file` | Search for packages that contain the specified file or path |
| `apt-file show\|list package` | List the contents of a specific package |
| `apt-file search\|find [-x\|--regexp] regex` | Search for packages that match the `regex` |
| `apt-file --help` | Show command usage and option reference |
| `man apt-file` | Open the full manual page |
| `whatis apt-file` | Print one-line command description |
| `type -a apt-file` | Show how the shell resolves the command path |
| `command -v apt-file` | Print executable path used by current shell |
| `tldr apt-file` | Show concise command examples |
| `apropos apt-file` | Search manual database for related commands |
| `apt-file --version` | Print local tool version |
