# cs4n Command Guides
A heavily expanded command cheats repo with practical workflows, safer defaults, and fast copy/paste snippets.

## New folder structure
- `guides/build/` - CMake/Make build workflows.
- `guides/cli/` - terminal workflow (`git`, `gh`, `rg`, `tmux`, `wget`).
- `guides/codex/` - Codex control templates and quality checklists.
- `guides/dev/` - language/framework loops (`python`, `flutter`, `cargo`).
- `guides/linux/` - daily Linux command cheats.
- `guides/pkg/` - package management (`apt`, `nala`, `aptitude`, `dpkg`, `npm`, `pip`, `uv`, `dart pub`).
- `guides/pkg/apt-family/` - per-command docs for the full `apt-*` family plus `add-apt-repository`.
- `guides/system/` - Docker and Compose operations.
- `guides/INDEX.md` - complete file map (all markdown files and locations).

## Start order
1. Read `guides/INDEX.md` for the full file map.
2. Read `guides/cli/github.md` for baseline Git/GitHub flow.
3. Read `guides/pkg/README.md` then `guides/pkg/apt-family/README.md` for package tooling.
4. Use specific command files when running tasks.

## Command syntax legend
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is short option form and `--long` is long option form.
- Prefer dry-run/inspect commands first, then apply commands.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `tree guides -L 2` | Visualize the top-level guide structure quickly |
| `find guides -type f -name '*.md' | sort` | List all markdown guides in sorted order |
| `rg -n '^## ' guides` | Scan all section headings across the guides |
| `rg -n 'apt-' guides/pkg` | Find all `apt-*` references in package docs |
| `rg -n 'Expanded Cheats' guides` | Verify expanded cheat sections across files |
| `ls -lah guides/pkg/apt-family` | Inspect full apt-family file set |
| `git status --short` | Review current repo changes quickly |
| `git diff -- guides` | Inspect content edits inside guides only |
| `git add guides README.md` | Stage structure + docs updates |
| `git commit -m 'Reorganize guides and massively expand cheats'` | Commit the documentation overhaul |
| `git push origin main` | Publish changes to remote |
| `code .` | Open repository in VS Code |
