# Extensions, Packages, and Repo Strategy (Ubuntu)
Recommendations focused on stability, performance, and maintainability.

## Editor extensions (VS Code)
- `GitLens` - deep git blame/history context.
- `Error Lens` - inline diagnostics visibility.
- `Even Better TOML` - better TOML editing (`pyproject.toml`, cargo files).
- `rust-analyzer` - Rust IDE support.
- `ms-python.python` + `ms-python.vscode-pylance` - Python workflow.
- `Dart-Code.dart-code` + `Dart-Code.flutter` - Flutter/Dart support.
- `mkhl.shfmt` and `timonwong.shellcheck` - shell quality.
- `EditorConfig.EditorConfig` - formatting consistency across repos.
- `streetsidesoftware.code-spell-checker` - docs/code typo reduction.

## CLI packages worth adding
- `fd` - faster, friendlier `find`.
- `bat` - syntax-aware `cat` replacement.
- `eza` - modern `ls` alternative.
- `zoxide` - smart directory jumping.
- `fzf` - fuzzy search for files/history/commands.
- `btop` - modern resource monitor alternative to `htop`.
- `jq` / `yq` - JSON/YAML scripting essentials.

## Better than random PPAs: preferred repo order
1. Official distro repos first (security updates and integration).
2. Official vendor repos for fast-moving tools (Docker, GitHub CLI, NodeSource, etc.).
3. Well-maintained PPAs only when the above cannot provide needed versions.

## PPAs/repo sources commonly useful (use intentionally)
- `ppa:git-core/ppa` - newer Git than default Ubuntu channels.
- `ppa:deadsnakes/ppa` - additional Python versions.
- Docker official apt repo - Docker Engine/CLI/Buildx/Compose plugin.
- GitHub CLI official apt repo - freshest `gh` releases.
- NodeSource apt repo - current Node major lines.
- Kitware apt repo - newer CMake on Ubuntu LTS.

## Decision rule for adding a new source
- Add only if you need a feature/version unavailable in distro repos.
- Pin package priorities to avoid accidental broad upgrades.
- Document why the source exists and who owns maintenance.

## Quick source-audit commands
- `grep -R "^deb " /etc/apt/sources.list /etc/apt/sources.list.d/`
- `apt-cache policy <package>`
- `apt list --upgradable`

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `code` | Start Visual Studio Code |
| `code path/to/file_or_directory1 path/to/file_or_directory2 ...` | Open specific files/directories |
| `code [-d\|--diff] path/to/file1 path/to/file2` | Compare two specific files |
| `code [-n\|--new-window] path/to/file_or_directory1 path/to/file_or_directory2 ...` | Open specific files/directories in a new window |
| `code --install\|uninstall-extension publisher.extension` | Install/uninstall a specific extension |
| `code [-s\|--status]` | Display diagnostic and process information about the running code window |
| `code --list-extensions --show-versions` | Print installed extensions with their versions |
| `sudo code --user-data-dir path/to/directory` | Start the editor as a superuser (root) while storing user data in a specific directory |
| `code --help` | Show command usage and option reference |
| `man code` | Open the full manual page |
| `whatis code` | Print one-line command description |
| `type -a code` | Show how the shell resolves the command path |
| `command -v code` | Print executable path used by current shell |
| `tldr code` | Show concise command examples |
| `apropos code` | Search manual database for related commands |
| `code --version` | Print local tool version |
| `sudo apt update` | Update the list of available packages and versions (recommended before running other `apt` commands) |
| `apt search package` | Search packages by name or description |
| `apt list package` | Search packages by name only (supports wildcards like `*`) |
| `apt show package` | Show detailed information about a package |
