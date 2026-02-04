# Python — common project workflow
# Use this for virtual envs, packaging, and scripts.

## Envs (venv)
- `python -m venv .venv` — create env
- `source .venv/bin/activate` — activate (Linux/macOS)
- `deactivate` — exit env

## Packaging
- `python -m build` — build sdist/wheel
- `python -m pip install -e .` — editable install
- `python -m pip install -r requirements.txt` — install deps

## Run
- `python -m pytest` — tests
- `python -m pip check` — verify deps
