# `add-apt-repository` cheat sheet
Adds a repository into the /etc/apt/sources.list or .

## Syntax
- Primary usage: `sudo add-apt-repository [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `add-apt-repository repository_spec` | Add a new `apt` repository |
| `add-apt-repository [-r\|--remove] repository_spec` | Remove an `apt` repository |
| `add-apt-repository --update repository_spec` | Update the package cache after adding a repository |
| `add-apt-repository [-s\|--enable-source] repository_spec` | Allow source packages to be downloaded from the repository |
| `add-apt-repository --help` | Show command usage and option reference |
| `man add-apt-repository` | Open the full manual page |
| `whatis add-apt-repository` | Print one-line command description |
| `type -a add-apt-repository` | Show how the shell resolves the command path |
| `command -v add-apt-repository` | Print executable path used by current shell |
| `tldr add-apt-repository` | Show concise command examples |
| `apropos add-apt-repository` | Search manual database for related commands |
| `add-apt-repository --version` | Print local tool version |
