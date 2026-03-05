# `apt-extracttemplates` cheat sheet
Utility to extract debconf config and templates fr.

## Syntax
- Primary usage: `sudo apt-extracttemplates [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-extracttemplates package.deb` | Extract debconf templates from a .deb into current dir |
| `apt-extracttemplates ./downloads/package.deb` | Extract templates from a local package path |
| `apt-extracttemplates *.deb` | Batch-extract templates from multiple downloaded packages |
| `apt-extracttemplates package.deb && ls -1 *.templates` | Generate and list produced template files |
| `apt-extracttemplates package.deb && less *.templates` | Inspect installer/debconf questions before deployment |
| `apt-extracttemplates --help` | Show available extraction options and output behavior |
| `man apt-extracttemplates` | Open the full manual page |
| `whatis apt-extracttemplates` | Print one-line command description |
| `type -a apt-extracttemplates` | Show how the shell resolves the command path |
| `command -v apt-extracttemplates` | Print executable path used by current shell |
| `tldr apt-extracttemplates` | Show concise command examples |
| `apropos apt-extracttemplates` | Search manual database for related commands |
| `apt-extracttemplates --version` | Print local tool version |
