# pip — Python package installer
# Use it inside virtual environments when you’re not using uv.

## Install / upgrade
- `python -m pip install <pkg>` — install package
- `python -m pip install -U <pkg>` — upgrade package
- `python -m pip install -r requirements.txt` — install from file
- `python -m pip install -e .` — editable install

## Freeze / check
- `python -m pip list` — list packages
- `python -m pip freeze > requirements.txt` — export lock
- `python -m pip check` — verify deps

## Cleanup
- `python -m pip cache purge` — clear cache
- `python -m pip uninstall <pkg>` — remove package
