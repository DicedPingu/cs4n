# `dpkg` — Debian package manager (low level)

`dpkg` installs, removes, and provides information about .deb packages. It operates locally on individual `.deb` files and is used by higher‑level tools (`apt`, `aptitude`). Use `sudo` for system-wide operations.

## Syntax & basics

* Basic usage: `sudo dpkg [options] package.deb` (for install) or `dpkg [options] packages` (for queries).
* It does not resolve dependencies automatically; combine with `apt-get` or `apt` for dependency resolution.

## 1) Installing & removing `.deb` packages

| Command | Purpose |
| --- | --- |
| `sudo dpkg -i package.deb` | Install or upgrade a local `.deb`. |
| `sudo dpkg --install package.deb` | Same as `-i`. |
| `sudo dpkg -r package` | Remove package (keep config files). |
| `sudo dpkg --remove package` | Equivalent to `-r`. |
| `sudo dpkg -P package` | Purge package and configuration files. |
| `sudo dpkg --purge package` | Equivalent to `-P`. |
| `sudo dpkg --configure package` | Configure an unpacked package. |
| `sudo dpkg --unpack package.deb` | Unpack package but do not configure. |
| `sudo dpkg --force-all -i package.deb` | Force install ignoring dependency/conflict checks (dangerous). |

## 2) Querying packages & files

| Command | Purpose |
| --- | --- |
| `dpkg -l` | List all installed packages. |
| `dpkg -l | grep apache` | Filter installed packages. |
| `dpkg -l package` | Show status of package. |
| `dpkg -s package` | Get detailed status and metadata. |
| `dpkg -L package` | List files installed by package. |
| `dpkg -S /usr/bin/vim` | Find which package owns a file. |
| `dpkg -p package` | Display package information (description, dependencies). |
| `dpkg --print-architecture` | Print system architecture (e.g., amd64). |
| `dpkg --print-foreign-architectures` | List enabled foreign architectures. |

## 3) Package archives & database

| Command | Purpose |
| --- | --- |
| `dpkg-deb -I package.deb` | Show info about the package file. |
| `dpkg-deb -c package.deb` | List contents of package file. |
| `dpkg-deb --info package.deb` | Another way to view package metadata. |
| `dpkg --clear-selections` | Clear selection statuses (dangerous). |
| `dpkg --set-selections < selections.txt` | Set package selection states from file. |
| `dpkg --get-selections > selections.txt` | Export selections (for backups). |
| `dpkg-query -W -f='${binary:Package}\n'` | List installed package names only. |

## 4) Miscellaneous operations

| Command | Purpose |
| --- | --- |
| `dpkg --audit` | Check for partially installed packages. |
| `dpkg --force-confold -i package.deb` | Keep old config files when upgrading. |
| `dpkg --force-confnew -i package.deb` | Use new config files when upgrading. |
| `dpkg --compare-versions 1.2 lt 1.3 && echo 'upgrade needed'` | Compare package version strings. |
| `dpkg-divert --add --rename --divert /usr/bin/foo.real /usr/bin/foo` | Divert a file (override with custom binary). |
| `dpkg-divert --list` | List all diverted files. |
| `dpkg-statoverride --add root root 0755 /usr/bin/foo` | Override permissions/ownership of a file. |
| `dpkg-statoverride --remove /usr/bin/foo` | Remove stat override. |

## 5) Tips & troubleshooting

* Use `apt install ./package.deb` instead of `dpkg -i` to handle dependencies automatically.
* If installation fails due to dependencies, run `sudo apt -f install` to fix missing dependencies.
* After using `dpkg --unpack`, run `sudo dpkg --configure -a` to finish configuration.
* The dpkg database is stored in `/var/lib/dpkg`; careful editing of these files can corrupt the package manager.
* `dpkg --listfiles package | less` is an alias for `dpkg -L package` if you forget the letter.
* Always verify the integrity and origin of local `.deb` files before installing. 
