# Package Manager Guides
Package install/update/pin/publish workflows for system and language ecosystems.

## Files and locations
- System package managers: `apt.md`, `nala.md`, `aptitude.md`, `dpkg.md`
- Full apt command family: `apt-family/README.md` and `apt-family/*.md`
- Node ecosystem: `npm.md`, `npm-pub.md`
- Python ecosystem: `pip.md`, `uv.md`
- Dart ecosystem: `pub.md`

## `apt-family` coverage
- Includes dedicated files for `apt-add-repository`, `apt-cache`, `apt-cacher-ng`, `apt-cdrom`, `apt-config`, `apt-cudf`, `apt-cudf-get`, `apt-extracttemplates`, `apt-file`, `apt-forktracer`, `apt-ftparchive`, `apt-get`, `apt-key`, `apt-manage`, `apt-mark`, `apt-move`, `apt-show-source`, `apt-show-versions`, `apt-sortpkgs`, `apt-src`, and `add-apt-repository`.

## Recommended order
1. `apt.md` then `nala.md`
2. `aptitude.md` and `dpkg.md` for lower-level/alternative flows
3. `apt-family/README.md` for per-command deep dives
4. language package guides (`npm`, `pip`, `uv`, `pub`)

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `sudo apt update` | Refresh package index |
| `sudo apt full-upgrade` | Upgrade with dependency transitions |
| `apt-cache policy <pkg>` | Check candidate/installed versions and origins |
| `apt-mark hold <pkg>` | Freeze package at current version |
| `sudo nala upgrade --download-only` | Pre-download upgrade payloads |
| `aptitude search '~i'` | List installed packages with aptitude query syntax |
| `dpkg -l | rg '^ii'` | Show installed packages from dpkg database |
| `apt-file search /usr/bin/<binary>` | Find which package ships a path |
| `npm ci` | Reproducible Node install from lockfile |
| `python -m pip install -r requirements.txt` | Install Python requirements file |
| `uv sync --frozen` | Strict lockfile install in uv workflow |
| `dart pub upgrade --major-versions` | Attempt major upgrades in Dart packages |
