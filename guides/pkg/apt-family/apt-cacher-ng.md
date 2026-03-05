# `apt-cacher-ng` cheat sheet
caching proxy for software package downloads.

## Syntax
- Primary usage: `sudo apt-cacher-ng [subcommand/options] [targets]`
- Use `--help` before destructive actions and prefer simulation flags where available.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo systemctl status apt-cacher-ng` | Check whether apt-cacher-ng service is running |
| `sudo apt-cacher-ng -c /etc/apt-cacher-ng ForeGround=1` | Run apt-cacher-ng in foreground for debugging |
| `apt-cacher-ng -h` | Show apt-cacher-ng runtime options |
| `curl -I http://localhost:3142/acng-report.html` | Check local apt-cacher-ng reporting endpoint |
| `sudo journalctl -u apt-cacher-ng -f` | Follow cache server logs in real time |
| `sudo systemctl restart apt-cacher-ng` | Restart cache service after config changes |
| `apt-cacher-ng --help` | Show command usage and option reference |
| `man apt-cacher-ng` | Open the full manual page |
| `whatis apt-cacher-ng` | Print one-line command description |
| `type -a apt-cacher-ng` | Show how the shell resolves the command path |
| `command -v apt-cacher-ng` | Print executable path used by current shell |
| `tldr apt-cacher-ng` | Show concise command examples |
| `apropos apt-cacher-ng` | Search manual database for related commands |
| `apt-cacher-ng --version` | Print local tool version |
