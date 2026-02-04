# uv — fast Python package manager + env tool
# Use it for per‑project envs, locking, and reproducible installs.

## 1) New project (ordered)
- `uv init` — create pyproject.toml
- `uv python pin 3.14.2` — pin interpreter for the repo
- `uv add <pkg>` — add dependency
- `uv lock` — resolve + lock
- `uv sync` — create env + install

## 2) Existing project
- `uv sync` — fastest path to working env
- `uv run <cmd>` — run inside env without activating

## 3) Add / remove / upgrade
- `uv add <pkg>` — add dep
- `uv add --dev <pkg>` — dev dep
- `uv remove <pkg>` — remove dep
- `uv lock --upgrade` — upgrade all deps
- `uv lock --upgrade-package <pkg>` — upgrade one

## 4) Git dependencies (latest commits)
- `uv add "mypkg @ git+https://github.com/org/repo@main"` — track latest on main
- `uv add "mypkg @ git+https://github.com/org/repo@<tag>"` — pin release tag
- `uv add "mypkg @ git+https://github.com/org/repo@<sha>"` — pin commit
- `uv lock --upgrade-package mypkg` — refresh git ref to latest commit
- `uv sync` — apply lock to env

## 5) Run options
- `uv run --locked <cmd>` — fail if lock is stale
- `uv run --frozen <cmd>` — no lock updates
- `uv run --no-sync <cmd>` — run without syncing

## 6) Pip‑compat
- `uv pip install -r requirements.txt` — install reqs
- `uv pip sync requirements.txt` — exact sync
- `uv pip compile requirements.in -o requirements.txt` — lock
- `uv pip install -e .` — editable install

## 7) Tools
- `uvx <tool>` — run tool in temp env
- `uv tool install <tool>` — install CLI
- `uv tool upgrade <tool>` — upgrade CLI

## 8) Python mgmt
- `uv python list` — available versions
- `uv python install <ver>` — install Python
- `uv python pin <ver>` — pin version
