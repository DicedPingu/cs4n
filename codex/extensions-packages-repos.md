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

