# Python - project workflow basics
Use it for environment setup, dependency install, testing, and packaging.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Fast start for a project
- `python -m venv .venv` - create virtual environment.
- `source .venv/bin/activate` - activate on Linux/macOS.
- `python -m pip install -U pip` - update installer.
- `python -m pip install -r requirements.txt` - install dependencies.

## Day-to-day development
- `python -m pytest -q` - run test suite.
- `python -m pip check` - dependency integrity check.
- `python -m pip list --outdated` - identify upgrade candidates.

## Packaging and distribution
- `python -m build` - create sdist and wheel.
- `python -m pip install -e .` - editable local install.
- `python -m twine check dist/*` - package metadata validation.

## Alternative toolchains
- Use `uv` for faster lock/sync workflows.
- Use `pipx` for isolated CLI tool installs.

## Version guidance
- Local check: `python --version`
- Prefer currently supported Python branches and align team projects on one minor version.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `python` | Start a REPL (interactive shell) |
| `python path/to/file.py` | Execute a specific Python file |
| `python -i path/to/file.py` | Execute a specific Python file and start a REPL |
| `python -c "expression"` | Execute a Python expression |
| `python -m module arguments` | Run the script of the specified library module |
| `python -m pip install package` | Install a package using `pip` |
| `python -m pdb path/to/file.py` | Interactively debug a Python script |
| `python -m http.server` | Start the built-in HTTP server on port 8000 in the current directory |
| `python --help` | Show command usage and option reference |
| `man python` | Open the full manual page |
| `whatis python` | Print one-line command description |
| `type -a python` | Show how the shell resolves the command path |
| `command -v python` | Print executable path used by current shell |
| `tldr python` | Show concise command examples |
| `apropos python` | Search manual database for related commands |
| `python --version` | Print local tool version |
