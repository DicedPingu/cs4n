# `apt` — modern package management frontend for Debian/Ubuntu

`apt` combines capabilities of `apt-get` and `apt-cache` into a user-friendly interface for searching, installing, upgrading, and removing packages. It wraps low‑level tools (`dpkg`) while adding repository management and caching features.

## Syntax & basics

* Use as `sudo apt <command> [options]` for modifying packages.
* `apt` commands support short options (`-y`, `-q`) and long options (`--yes`, `--quiet`).
* `apt` stores downloaded packages in `/var/cache/apt/archives`.

## 1) Updating & upgrading

| Command | Purpose |
| --- | --- |
| `sudo apt update` | Fetch package lists from repositories. |
| `sudo apt upgrade` | Upgrade installed packages (no removals). |
| `sudo apt full-upgrade` | Upgrade packages and remove/install as needed. |
| `sudo apt dist-upgrade` | Synonym for `full-upgrade` (older usage). |
| `sudo apt autoremove` | Remove automatically installed packages no longer needed. |
| `sudo apt autoclean` | Remove outdated package files. |
| `sudo apt clean` | Clear package cache (remove all downloaded files). |
| `sudo apt upgrade --with-new-pkgs` | Install new dependencies while upgrading. |
| `sudo apt upgrade --fix-broken` | Fix dependency problems (run after interrupted operations). |

## 2) Installing & removing packages

| Command | Purpose |
| --- | --- |
| `sudo apt install firefox` | Install a package with dependencies. |
| `sudo apt install pkg=1.2.3` | Install specific version. |
| `sudo apt install ./package.deb` | Install local .deb file. |
| `sudo apt install -f` | Attempt to fix broken dependencies during install. |
| `sudo apt install --no-install-recommends pkg` | Skip recommended packages. |
| `sudo apt remove package` | Remove package but keep config files. |
| `sudo apt purge package` | Remove package and config files. |
| `sudo apt reinstall package` | Reinstall package. |
| `sudo apt install package1 package2` | Install multiple packages. |
| `sudo apt download package` | Download .deb file to current dir. |

## 3) Searching & information

| Command | Purpose |
| --- | --- |
| `apt search nginx` | Search packages names/descriptions. |
| `apt list --installed` | List installed packages. |
| `apt list --upgradable` | Show packages with available updates. |
| `apt show package` | Display package details (version, description, dependencies, origin). |
| `apt policy package` | Show installed and candidate versions and origin repository. |
| `apt-cache depends package` | Show dependencies. |
| `apt-cache rdepends package` | Show reverse dependencies. |
| `apt-cache madison package` | Display package versions across repositories. |

## 4) Repository & key management

| Command | Purpose |
| --- | --- |
| `sudo apt-add-repository ppa:ppa-name/ppa` | Add a PPA repository. |
| `sudo add-apt-repository 'deb http://example.com/debian stable main'` | Add custom repository. |
| `sudo apt-key add keyfile.gpg` | Add a repository GPG key (deprecated; use keyring). |
| `sudo apt-key list` | List trusted keys. |
| `sudo apt-key del <keyid>` | Remove key. |
| `sudo apt update --allow-releaseinfo-change` | Accept repository metadata changes. |
| `sudo apt update --list-cleanup` | Remove invalid entries from lists. |
| `sudo apt-mark hold package` | Hold package at current version. |
| `sudo apt-mark unhold package` | Unhold package. |
| `apt-cache policy` | Show repository priority pinning. |

## 5) Configuration & preferences

| Command | Purpose |
| --- | --- |
| `apt-config dump` | Show apt configuration. |
| `cat /etc/apt/sources.list` | View repository list. |
| `ls /etc/apt/sources.list.d` | Additional sources lists. |
| `sudo nano /etc/apt/sources.list` | Edit repository file. |
| `sudo apt edit-sources` | Open sources list in editor. |
| `apt preferences` | Use `/etc/apt/preferences` to pin package versions. |

## 6) Troubleshooting & advanced use

| Command | Purpose |
| --- | --- |
| `sudo apt install --fix-missing` | Attempt to correct missing packages. |
| `sudo dpkg --configure -a` | Configure unpacked packages (resolve after broken install). |
| `sudo apt-get check` | Verify that no packages are missing dependencies. |
| `sudo apt-get -o Debug::pkgProblemResolver=yes dist-upgrade` | Show dependency resolution process. |
| `sudo apt-get build-dep package` | Install build dependencies for a source package. |
| `sudo apt source package` | Download source package. |
| `sudo apt purge $(dpkg -l | awk '/^rc/ {print $2}')` | Purge leftover config files. |

## Tips

* Use `apt` for everyday package management. For scripting, `apt-get` is more stable across versions.
* Combine `apt update && apt upgrade` to refresh and upgrade in one line.
* When adding repositories, ensure they are trustworthy to avoid compromised packages.
* Avoid mixing apt with other packaging systems (snap, flatpak) unless you know how they interact.
