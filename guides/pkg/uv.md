# uv - fast Python package manager and environment tool
Use it for reproducible Python projects, lockfiles, and tool execution.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## New project (recommended order)
- `uv init` - create `pyproject.toml`.
- `uv python pin 3.14` - pin interpreter for this repo.
- `uv add <pkg>` - add dependency.
- `uv lock` - resolve and write lockfile.
- `uv sync` - create/update environment from lockfile.

## Existing project
- `uv sync` - fastest path to a working env.
- `uv run <cmd>` - run in project environment without manual activation.
- `uv run --locked <cmd>` - fail if lockfile is stale.

## Dependency management
- `uv add --dev <pkg>` - add dev dependency group.
- `uv remove <pkg>` - remove dependency.
- `uv lock --upgrade` - upgrade all resolvable dependencies.
- `uv lock --upgrade-package <pkg>` - upgrade one dependency.

## Git dependencies and pin strategy
- `uv add "mypkg @ git+https://github.com/org/repo@main"` - track a branch (fast, less stable).
- `uv add "mypkg @ git+https://github.com/org/repo@<tag>"` - pin release tag.
- `uv add "mypkg @ git+https://github.com/org/repo@<sha>"` - pin exact commit (most reproducible).
- `uv lock --upgrade-package mypkg` - move git ref forward.

## Pip-compat and tools
- `uv pip compile requirements.in -o requirements.txt` - compile constraints.
- `uv pip sync requirements.txt` - exact sync from requirements.
- `uvx ruff check .` - run a tool in an ephemeral environment.
- `uv tool install ruff` - persistent global-ish tool install.

## Version and release line
- Local check: `uv --version`
- Upstream release snapshot: uv `0.10.0` (2026-02-08 snapshot).
- Official release tracking: `astral-sh/uv` releases.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `uv init` | Create a new Python project in the current directory |
| `uv init path/to/directory` | Create a new Python project at the specified path |
| `uv add package` | Add a new dependency to the project |
| `uv remove package` | Remove a dependency from the project |
| `uv run path/to/script.py` | Run a script in the project's environment |
| `uv run command` | Run a command in the project's environment |
| `uv sync` | Update a project's environment from `pyproject.toml` |
| `uv lock` | Create a lock file for the project's dependencies |
| `uv --help` | Show command usage and option reference |
| `man uv` | Open the full manual page |
| `whatis uv` | Print one-line command description |
| `type -a uv` | Show how the shell resolves the command path |
| `command -v uv` | Print executable path used by current shell |
| `tldr uv` | Show concise command examples |
| `apropos uv` | Search manual database for related commands |
| `uv --version` | Print local tool version |
