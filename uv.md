# uv (Practical Workflow Cheatsheet)

## 1) New project (ordered)
1) `uv init`
2) `uv python pin 3.14.2` (or required version)
3) `uv add <package>`
4) `uv lock`
5) `uv sync`
6) `uv run <command>`

## 2) Existing project (ordered)
- `uv sync` (fastest way to get a working env)
- `uv run <command>`

## 3) Add / remove / upgrade deps
- `uv add <package>`
- `uv add --dev <package>`
- `uv remove <package>`
- `uv lock --upgrade`
- `uv lock --upgrade-package <package>`

## 4) Run commands
- `uv run <command>`
- `uv run --locked <command>`
- `uv run --frozen <command>`
- `uv run --no-sync <command>`

## 5) Virtual envs
- `uv venv`
- `uv venv --python 3.12`
- `source .venv/bin/activate`

## 6) Pip‑compat mode
- `uv pip install -r requirements.txt`
- `uv pip sync requirements.txt`
- `uv pip compile requirements.in -o requirements.txt`
- `uv pip list | uv pip check | uv pip tree`

## 7) Tools
- `uvx <tool>`
- `uv tool install <tool>`
- `uv tool upgrade <tool>`
- `uv tool list`

## 8) Python management
- `uv python list`
- `uv python install <version>`
- `uv python pin <version>`
- `uv python find`

## 9) Cache / self
- `uv cache clean`
- `uv self update`
