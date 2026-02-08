# Version Sources Snapshot
Reference snapshot date: `2026-02-08`.

## Core package managers and runtimes
- npm `v11.9.0` - https://api.github.com/repos/npm/cli/releases/latest - local check: `npm --version`
- Node LTS `v24.13.0` (npm `11.6.2`) - https://nodejs.org/dist/index.json - local check: `node --version`
- uv `0.10.0` - https://api.github.com/repos/astral-sh/uv/releases/latest - local check: `uv --version`
- pip `26.0.1` - https://pypi.org/pypi/pip/json - local check: `python -m pip --version`
- Dart stable `3.10.9` - https://storage.googleapis.com/dart-archive/channels/stable/release/latest/VERSION - local check: `dart --version`
- Flutter stable `3.38.9` - https://storage.googleapis.com/flutter_infra_release/releases/releases_linux.json - local check: `flutter --version`

## Dev and build tools
- Git `2.53.0` - https://mirrors.edge.kernel.org/pub/software/scm/git/ - local check: `git --version`
- GitHub CLI `v2.86.0` - https://api.github.com/repos/cli/cli/releases/latest - local check: `gh --version`
- ripgrep `15.1.0` - https://api.github.com/repos/BurntSushi/ripgrep/releases/latest - local check: `rg --version`
- tmux `3.6a` - https://api.github.com/repos/tmux/tmux/releases/latest - local check: `tmux -V`
- CMake `v4.2.3` - https://api.github.com/repos/Kitware/CMake/releases/latest - local check: `cmake --version`
- GNU Make `4.4.1` - https://ftp.gnu.org/gnu/make/ - local check: `make --version`
- Rust/Cargo line `1.93.0` - https://static.rust-lang.org/dist/channel-rust-stable.toml - local check: `cargo --version`

## System/container tools
- Docker Engine `docker-v29.2.1` - https://api.github.com/repos/moby/moby/releases/latest - local check: `docker version`
- Docker Compose `v5.0.2` - https://api.github.com/repos/docker/compose/releases/latest - local check: `docker compose version`
- systemd `v259.1` - https://api.github.com/repos/systemd/systemd/releases/latest - local check: `systemctl --version`
- OpenSSH `9.9p2` - https://www.openssh.com/releasenotes.html - local check: `ssh -V`
- curl `8.18.0` - https://curl.se/download.html - local check: `curl --version`
- fwupd `2.0.19` - https://api.github.com/repos/fwupd/fwupd/releases/latest - local check: `fwupdmgr --version`
- htop `3.4.1` - https://api.github.com/repos/htop-dev/htop/releases/latest - local check: `htop --version`
- rsync `3.4.1` - https://download.samba.org/pub/rsync/ - local check: `rsync --version`

## GNU utilities used by Linux guides
- coreutils `9.10` (cat/chmod/chown/head/tail/ls/mkdir/mv/touch) - https://ftp.gnu.org/gnu/coreutils/
- findutils `4.10.0` (find/xargs) - https://ftp.gnu.org/gnu/findutils/
- gawk `5.3.2` - https://ftp.gnu.org/gnu/gawk/
- grep `3.12` - https://ftp.gnu.org/gnu/grep/
- sed `4.9` - https://ftp.gnu.org/gnu/sed/
- tar `1.35` - https://ftp.gnu.org/gnu/tar/
- wget `1.25.0` - https://ftp.gnu.org/gnu/wget/

