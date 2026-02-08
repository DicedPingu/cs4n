# pip - Python package installer
# Use it inside a virtual environment when you are not using uv/poetry.

## Baseline workflow
- `python -m venv .venv && source .venv/bin/activate` - isolate project environment.
- `python -m pip install -U pip` - update installer first.
- `python -m pip install <pkg>` - add dependency.
- `python -m pip install -r requirements.txt` - install from constraints file.

## Build/install modes
- `python -m pip install -e .` - editable local package install.
- `python -m pip install .` - regular local package install.
- `python -m pip install --no-deps <wheel.whl>` - install artifact without resolver side effects.

## Inspection and reproducibility
- `python -m pip list --outdated` - see candidates for upgrades.
- `python -m pip freeze > requirements.txt` - pin current environment.
- `python -m pip check` - detect broken dependency graph.
- `python -m pip index versions <pkg>` - inspect available versions.

## Cleanup and cache
- `python -m pip uninstall <pkg>` - remove package.
- `python -m pip cache dir` - show cache path.
- `python -m pip cache purge` - clear cache artifacts.

## Version and release line
- Local check: `python -m pip --version`
- Upstream release snapshot: pip `26.0.1` (2026-02-08 snapshot).
- Official source: PyPI project metadata for `pip`.

