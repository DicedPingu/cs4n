# Guides
Practical command guides with ordered workflows, safe defaults, and upgrade-aware notes.

## Start Here (if you're green)
- New to git? Read `cli/github.md` first.
- Follow sections in order: `1) One-time setup` -> `2) Get a repo` -> `3) Daily workflow`.
- Keep this rule: pull before coding, push after each finished chunk.

## Layout
- `cli/` - GitHub workflow (`git` + `gh`) including Pop!_OS/Android/AI patterns, plus terminal productivity tooling.
- `cli/github.md` - canonical Git + GitHub CLI workflow.
- `pkg/` - package manager workflows (`npm`, `uv`, `pip`, `dart pub`).
- `dev/` - language and framework flows (`python`, `flutter`, `cargo`).
- `build/` - build systems (`make`, `cmake`).
- `system/` - containers and compose orchestration.
- `linux/` - daily Linux command references.
- `codex/` - how to control Codex behavior and outputs.
- Folder indexes: `build/README.md`, `cli/README.md`, `dev/README.md`, `linux/README.md`, `pkg/README.md`, `system/README.md`.

## Command syntax legend
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short option; `--long` is the long form.
- Always run preview/dry-run variants first when provided.

## Code Insiders note
- Open repo in editor from terminal with `code .`.
- If you prefer the name `code-insiders`, add: `alias code-insiders='code'`.

## How these files are structured
- Header: one-line purpose + when to use it.
- Main flow first: commands in the order most people actually run them.
- Options nearby: flags are grouped next to the workflow they affect.
- Safer alternatives: destructive patterns are paired with dry-run checks.
- Version awareness: each moving tool includes a local version check and upstream release pointer.

## Version snapshot date
- Release references were refreshed on `2026-02-08`.
