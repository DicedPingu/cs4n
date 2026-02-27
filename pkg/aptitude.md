# `aptitude` — interactive APT frontend with sophisticated dependency resolution

`aptitude` offers a command‑line and text‑user-interface for package management on Debian/Ubuntu. It provides advanced search, safe upgrades, flexible dependency handling, and an ncurses UI.

## Launching

| Command | Purpose |
| --- | --- |
| `sudo aptitude` | Start ncurses UI. |
| `sudo aptitude update` | Update package lists (same as `apt update`). |
| `sudo aptitude upgrade` | Perform a safe system upgrade. |
| `sudo aptitude full-upgrade` | Perform a full/dist upgrade (may remove packages). |
| `sudo aptitude --help` | Show basic help. |
| `aptitude search ~` | Use search patterns (see below) outside UI. |

## Installing & removing packages

| Command | Purpose |
| --- | --- |
| `sudo aptitude install vim` | Install a package. |
| `sudo aptitude install pkg1 pkg2` | Install multiple packages. |
| `sudo aptitude install '?reverse-depends(package)'` | Install packages that depend on a given package. |
| `sudo aptitude remove vim` | Remove package but keep config files. |
| `sudo aptitude purge vim` | Remove package and purge configuration. |
| `sudo aptitude reinstall openssh-server` | Reinstall package. |
| `sudo aptitude hold nginx` | Hold package at current version (prevent upgrades). |
| `sudo aptitude unhold nginx` | Remove hold. |
| `sudo aptitude download package` | Download .deb file to current dir. |

## Searching packages using patterns

Aptitude uses a powerful pattern language. Some examples:

| Pattern | Description |
| --- | --- |
| `~n^lib` | Packages whose names start with `lib`. |
| `~dpython` | Descriptions containing “python”. |
| `~i` | Installed packages. |
| `~U` | Packages with upgrades available. |
| `~pstandard` | Packages with priority standard. |
| `~aamd64` | Architecture-specific packages (amd64). |
| `~sunstable` | From unstable suite (depends on sources). |
| `?reverse-depends(vim)` | Packages that depend on vim. |
| `?obsolete` | Obsolete/local packages. |

Use these patterns with `aptitude search` or within the UI’s search bar.

## Working with the ncurses UI

In the UI:

* Use **arrow keys** to navigate categories and packages.
* Press `Enter` to expand/collapse package lists.
* Press `+` to mark a package for installation, `-` for removal, `=` for hold.
* Press `g` to view the action preview, then `g` again to execute.
* Use `/` to search; press `n`/`p` to move between results.
* Press `u` to update package list, `U` to mark upgrades.
* Press `q` to quit or return to previous screen.
* Press `F` to display filter (use patterns like `~U` for upgradable).
* Toggle views with `l` (package states), `v` (versions), `t` (task view).

## Advanced dependency resolution

During installation/removal, aptitude proposes solutions when conflicts arise. Use:

| Command | Purpose |
| --- | --- |
| Press `e` in UI | Examine dependency problems. |
| Press `.` and `,` | Cycle through alternate solutions. |
| Press `!` | Accept the current solution. |
| `sudo aptitude safe-upgrade` | Upgrade packages while minimizing changes. |
| `sudo aptitude full-upgrade` | Perform upgrades even if it involves removing packages. |

## Miscellaneous commands

| Command | Purpose |
| --- | --- |
| `aptitude show package` | Detailed package info. |
| `aptitude versions package` | Show available versions across repositories. |
| `aptitude changelog package` | View Debian changelog. |
| `aptitude why package` | Explain why a package is installed. |
| `aptitude why-not package` | Why a package cannot be installed. |
| `sudo aptitude keep-all` | Mark all packages as manually installed (disable auto-remove). |
| `sudo aptitude forget-new` | Mark all new packages as seen. |
| `sudo aptitude create-state-bundle bundle.tar.gz` | Create backup of installed state. |
| `sudo aptitude clean` | Clean the local repository of retrieved package files. |
| `sudo aptitude autoclean` | Remove packages that can no longer be downloaded. |

## Tips

* Aptitude uses the same package lists and cache as apt; you can safely switch between them.
* The pattern language is powerful; combine flags: e.g., `aptitude search '~i!~M'` shows installed packages not automatically installed.
* Use `aptitude moo` for Easter eggs.
* You can use aptitude non-interactively in scripts, but note that the UI may propose complex solutions; use `-y` for automatic yes.
