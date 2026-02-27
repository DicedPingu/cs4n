# `nala` — user‑friendly front‑end for APT

`nala` wraps `apt` and `apt-get`, providing a cleaner interface, better progress bars, parallel downloads, history management, and easier package searches. It works on Debian-based systems (Ubuntu, Mint, Pop!_OS).

## Installation & basics

* Install `nala` via apt: `sudo apt install nala` (if available on your distro).
* Command syntax: `sudo nala <command> [options] [packages...]`
* Most commands accept `--assume-yes` (`-y`) to auto-confirm.

## 1) Updating & upgrading

| Command | Purpose |
| --- | --- |
| `sudo nala update` | Refresh package index (like `apt update`). |
| `sudo nala upgrade` | Upgrade all installed packages (standard safe upgrade). |
| `sudo nala upgrade --purge` | Remove obsolete packages during upgrade. |
| `sudo nala upgrade --yes` | Upgrade non-interactively. |
| `sudo nala upgrade --install-recommends` | Include recommended packages. |
| `sudo nala autoremove` | Remove unneeded dependencies (like `apt autoremove`). |
| `sudo nala autopurge` | Autoremove plus purge configuration files of removed packages. |

## 2) Installing & removing packages

| Command | Purpose |
| --- | --- |
| `sudo nala install htop` | Install `htop` and dependencies. |
| `sudo nala install package1 package2` | Install multiple packages at once. |
| `sudo nala install ./file.deb` | Install a local `.deb` file. |
| `sudo nala remove nano` | Uninstall package but keep config files. |
| `sudo nala purge nano` | Uninstall and purge configuration files. |
| `sudo nala reinstall nginx` | Reinstall package (handy for repair). |
| `sudo nala install nala-legacy` | Example: switch from nala 2.x to legacy UI. |
| `sudo nala install --no-install-recommends pkg` | Skip recommended dependencies. |

## 3) Searching & info

| Command | Purpose |
| --- | --- |
| `nala search ssh` | Search packages whose names/descriptions match “ssh”. |
| `nala search --details python3-requests` | Show detailed package info. |
| `nala show docker` | Display package details and dependencies. |
| `nala list` | List all installed packages. |
| `nala list pkgname` | Check if specific package is installed. |
| `nala list --installed` | List installed packages (alias for `list`). |
| `nala list --upgradable` | List packages with available upgrades. |
| `nala history` | View transaction history (install/remove/upgrade). |
| `nala history undo <id>` | Undo a transaction by history ID. |

## 4) Repo & mirror management

| Command | Purpose |
| --- | --- |
| `nala sources` | Show current repository sources. |
| `sudo nala fetch` | Refresh sources and create mirror list based on speed. |
| `sudo nala gen-mirrors` | Generate new mirrors list for your country/region. |
| `sudo nala gen-mirrors --country NO` | Generate mirror list for Norway. |
| `sudo nala gen-mirrors --source debian` | Choose distro source (debian, ubuntu). |
| `sudo nala fetch --choose` | Interactively select mirrors. |
| `nala mirror-history` | Show mirror changes history. |

## 5) Configuration & diagnostics

| Command | Purpose |
| --- | --- |
| `nala --version` | Show nala version. |
| `nala --help` | Display help for commands. |
| `nala --no-colors` | Disable colored output. |
| `nala --assume-yes install pkg` | Always answer yes. |
| `nala --non-interactive upgrade` | Run upgrade without prompts (implies `--assume-yes`). |
| `nala fetch --debug` | Show debug info when fetching mirrors. |
| `nala history list` | Alias for `history`. |
| `nala history redo <id>` | Redo a previously undone transaction. |
| `nala profile list` | List saved profiles (config sets). |
| `nala profile load minimal` | Load minimal profile (customizable). |
| `nala profile save myprefs` | Save current preferences as `myprefs`. |

## 6) Advanced & scriptable options

| Command | Purpose |
| --- | --- |
| `nala install --download-only pkg` | Download package but don’t install. |
| `nala upgrade --dry-run` | Show what would be upgraded without changing anything. |
| `nala install --simulate pkg` | Simulate installation. |
| `nala install --tab` | Show install progress with a tabbed interface (nala 2.x). |
| `nala update --no-progress` | Run update without progress bar. |
| `nala upgrade --override-anything` | Override pinned packages (dangerous). |
| `nala purge --autoremove pkg` | Remove package and unneeded dependencies. |
| `sudo nala shell` | Drop into an interactive root shell using nala’s environment. |

## Tips

* Nala stores transaction history; use `nala history` to inspect or undo operations.
* Use `nala fetch` or `nala gen-mirrors` to speed up downloads by choosing fast mirrors.
* Combine `nala` with `apt-mark hold` to pin packages (nala respects APT’s hold status).
* To switch back to apt, simply use `apt` normally—nala does not replace apt.
