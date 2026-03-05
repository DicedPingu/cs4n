# `apt-ftparchive` cheat sheet
Utility to generate index files.

## Syntax
- Primary usage: `sudo apt-ftparchive [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-ftparchive packages pool/` | Generate Packages metadata for a repository pool |
| `apt-ftparchive sources pool/` | Generate Sources metadata for source packages |
| `apt-ftparchive release dists/stable > dists/stable/Release` | Generate Release metadata for a repository |
| `apt-ftparchive contents pool/ > Contents-amd64` | Build a Contents index for file-to-package lookup |
| `apt-ftparchive generate apt-ftparchive.conf` | Run archive generation using a config file |
| `apt-ftparchive clean apt-ftparchive.conf` | Clean generated DB/cache files for archive metadata |
| `apt-ftparchive --help` | Show command usage and option reference |
| `man apt-ftparchive` | Open the full manual page |
| `whatis apt-ftparchive` | Print one-line command description |
| `type -a apt-ftparchive` | Show how the shell resolves the command path |
| `command -v apt-ftparchive` | Print executable path used by current shell |
| `tldr apt-ftparchive` | Show concise command examples |
| `apropos apt-ftparchive` | Search manual database for related commands |
| `apt-ftparchive --version` | Print local tool version |
