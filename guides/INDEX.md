# Guides File Index
Authoritative map of where every markdown guide lives after the reorganization.

## `build/`
- `guides/build/README.md`
- `guides/build/cmake.md`
- `guides/build/make.md`

## `cli/`
- `guides/cli/README.md`
- `guides/cli/github.md`
- `guides/cli/rg.md`
- `guides/cli/tmux.md`
- `guides/cli/wget.md`

## `codex/`
- `guides/codex/README.md`
- `guides/codex/control-profiles.md`
- `guides/codex/extensions-packages-repos.md`
- `guides/codex/request-template.md`
- `guides/codex/review-checklist.md`
- `guides/codex/version-sources.md`
- `guides/codex/workflow-rules.md`

## `dev/`
- `guides/dev/README.md`
- `guides/dev/cargo.md`
- `guides/dev/flutter-pub.md`
- `guides/dev/flutter.md`
- `guides/dev/python.md`

## `linux/`
- `guides/linux/README.md`
- `guides/linux/awk.md`
- `guides/linux/cat.md`
- `guides/linux/chmod_chown.md`
- `guides/linux/curl.md`
- `guides/linux/find.md`
- `guides/linux/fwupd.md`
- `guides/linux/grep.md`
- `guides/linux/head_tail.md`
- `guides/linux/htop.md`
- `guides/linux/journalctl.md`
- `guides/linux/ls.md`
- `guides/linux/mkdir.md`
- `guides/linux/mv.md`
- `guides/linux/rsync.md`
- `guides/linux/sed.md`
- `guides/linux/ssh.md`
- `guides/linux/systemctl.md`
- `guides/linux/tar.md`
- `guides/linux/touch.md`
- `guides/linux/xargs.md`

## `pkg/`
- `guides/pkg/README.md`
- `guides/pkg/apt-family/README.md`
- `guides/pkg/apt-family/add-apt-repository.md`
- `guides/pkg/apt-family/apt-add-repository.md`
- `guides/pkg/apt-family/apt-cache.md`
- `guides/pkg/apt-family/apt-cacher-ng.md`
- `guides/pkg/apt-family/apt-cdrom.md`
- `guides/pkg/apt-family/apt-config.md`
- `guides/pkg/apt-family/apt-cudf-get.md`
- `guides/pkg/apt-family/apt-cudf.md`
- `guides/pkg/apt-family/apt-extracttemplates.md`
- `guides/pkg/apt-family/apt-file.md`
- `guides/pkg/apt-family/apt-forktracer.md`
- `guides/pkg/apt-family/apt-ftparchive.md`
- `guides/pkg/apt-family/apt-get.md`
- `guides/pkg/apt-family/apt-key.md`
- `guides/pkg/apt-family/apt-manage.md`
- `guides/pkg/apt-family/apt-mark.md`
- `guides/pkg/apt-family/apt-move.md`
- `guides/pkg/apt-family/apt-show-source.md`
- `guides/pkg/apt-family/apt-show-versions.md`
- `guides/pkg/apt-family/apt-sortpkgs.md`
- `guides/pkg/apt-family/apt-src.md`
- `guides/pkg/apt.md`
- `guides/pkg/aptitude.md`
- `guides/pkg/dpkg.md`
- `guides/pkg/nala.md`
- `guides/pkg/npm-pub.md`
- `guides/pkg/npm.md`
- `guides/pkg/pip.md`
- `guides/pkg/pub.md`
- `guides/pkg/uv.md`

## `system/`
- `guides/system/README.md`
- `guides/system/docker-compose.md`
- `guides/system/docker.md`

## Quick checks
- `find guides -type f -name '*.md' | wc -l` - count guide files.
- `rg -n '^# ' guides` - list top-level headings.
- `rg -n 'apt-' guides/pkg` - inspect apt-family coverage.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `find guides -type f -name '*.md' | sort` | List all guide files in deterministic order |
| `find guides -type f -name '*.md' | wc -l` | Count total markdown guides |
| `rg -n '^# ' guides` | Show all top-level headings |
| `rg -n '^## ' guides/pkg/apt-family` | Audit section structure in apt-family files |
| `rg -n 'sudo apt' guides/pkg` | Find sudo apt examples across package docs |
| `rg -n 'docker compose' guides/system` | Locate compose-specific operations quickly |
| `rg -n 'Expanded Cheats' guides | wc -l` | Verify expanded cheat sections coverage |
| `git ls-files 'guides/**/*.md' | wc -l` | Count tracked guide files in git index |
| `git diff --name-only -- guides` | Show changed guide files |
| `git log --oneline -- guides | head -n 20` | Quick history summary for docs tree |
| `tree guides -L 3` | Visualize directory hierarchy with depth limit |
| `code guides` | Open the guides subtree in your editor |
