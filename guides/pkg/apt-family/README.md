# APT Family Command Set
Focused cheat sheets for `apt-*` and related repository/source commands.

## Included command files
- `apt-add-repository` -> `apt-add-repository.md`
- `apt-cache` -> `apt-cache.md`
- `apt-cacher-ng` -> `apt-cacher-ng.md`
- `apt-cdrom` -> `apt-cdrom.md`
- `apt-config` -> `apt-config.md`
- `apt-cudf` -> `apt-cudf.md`
- `apt-cudf-get` -> `apt-cudf-get.md`
- `apt-extracttemplates` -> `apt-extracttemplates.md`
- `apt-file` -> `apt-file.md`
- `apt-forktracer` -> `apt-forktracer.md`
- `apt-ftparchive` -> `apt-ftparchive.md`
- `apt-get` -> `apt-get.md`
- `apt-key` -> `apt-key.md`
- `apt-manage` -> `apt-manage.md`
- `apt-mark` -> `apt-mark.md`
- `apt-move` -> `apt-move.md`
- `apt-show-source` -> `apt-show-source.md`
- `apt-show-versions` -> `apt-show-versions.md`
- `apt-sortpkgs` -> `apt-sortpkgs.md`
- `apt-src` -> `apt-src.md`
- `add-apt-repository` -> `add-apt-repository.md`

## Practical flow
1. Use `apt-get.md`, `apt-cache.md`, and `apt-mark.md` for core package lifecycle work.
2. Use `apt-file.md` and `apt-show-versions.md` for diagnostics and audits.
3. Use archive/repository tools (`apt-ftparchive.md`, `apt-sortpkgs.md`) for mirror/repo management.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `ls -1 guides/pkg/apt-family/*.md` | List all apt-family cheat files |
| `rg -n '^# ' guides/pkg/apt-family/*.md` | Verify each file has a command title |
| `rg -n 'deprecated' guides/pkg/apt-family` | Locate deprecation notes (`apt-key`, etc.) |
| `sed -n '1,80p' guides/pkg/apt-family/apt-get.md` | Preview apt-get cheat header and syntax |
| `sed -n '1,80p' guides/pkg/apt-family/apt-cache.md` | Preview apt-cache cheat header and syntax |
| `rg -n 'apt-mark' guides/pkg/apt-family` | Find hold/unhold related docs quickly |
| `rg -n 'repository|mirror|archive' guides/pkg/apt-family` | Jump to repo and mirror tooling docs |
| `find guides/pkg/apt-family -type f -name '*.md' | wc -l` | Count apt-family command files |
| `git diff -- guides/pkg/apt-family` | Review only apt-family changes |
| `git add guides/pkg/apt-family` | Stage apt-family updates |
| `git commit -m 'Expand apt-family command cheats'` | Commit apt-family documentation updates |
| `git push origin main` | Publish apt-family docs changes |
