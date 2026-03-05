# `apt-sortpkgs` cheat sheet
Utility to sort package index files.

## Syntax
- Primary usage: `sudo apt-sortpkgs [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `apt-sortpkgs Packages > Packages.sorted` | Sort package index records into canonical order |
| `apt-sortpkgs Sources > Sources.sorted` | Sort source index records consistently |
| `apt-sortpkgs Packages.gz > Packages.sorted` | Sort and normalize index records from compressed input |
| `apt-sortpkgs < Packages > Packages.out` | Run as a filter in shell pipelines |
| `apt-sortpkgs --help` | Inspect sorting behavior and available options |
| `zcat Packages.gz \| apt-sortpkgs > Packages.sorted` | Normalize index files in CI/repo automation |
| `man apt-sortpkgs` | Open the full manual page |
| `whatis apt-sortpkgs` | Print one-line command description |
| `type -a apt-sortpkgs` | Show how the shell resolves the command path |
| `command -v apt-sortpkgs` | Print executable path used by current shell |
| `tldr apt-sortpkgs` | Show concise command examples |
| `apropos apt-sortpkgs` | Search manual database for related commands |
| `apt-sortpkgs --version` | Print local tool version |
