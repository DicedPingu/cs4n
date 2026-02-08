# npm - JavaScript/Node package manager
# Use it to install dependencies, run scripts, and publish packages.

## Most common workflow
- `npm init -y` - scaffold `package.json` quickly.
- `npm install` - install dependencies from lockfile/package.
- `npm install <pkg>` - add runtime dependency.
- `npm install -D <pkg>` - add dev dependency.
- `npm run <script>` - execute a project script.

## Reproducible installs and CI
- `npm ci` - strict lockfile install (best for CI).
- `npm ci --omit=dev` - production-only CI image install.
- `npm install --save-exact <pkg>` - pin exact version.
- `npm pkg set engines.node=">=24"` - communicate supported Node range.

## Updating without chaos
- `npm outdated` - see what changed upstream.
- `npm update` - update within semver ranges.
- `npm update <pkg>` - upgrade one dependency.
- `npm dedupe` - reduce duplicate dependency tree entries.
- `npm prune` - remove extraneous modules.

## Scripts, binaries, and local CLIs
- `npm run` - list available scripts.
- `npm run <script> -- <args>` - pass through arguments.
- `npm exec <cmd>` - run local package binaries.
- `npx <cmd>` - one-off command execution (alias around npm exec behavior).

## Security and supply chain checks
- `npm audit` - vulnerability report.
- `npm audit fix` - apply non-breaking fixes.
- `npm audit fix --force` - include potentially breaking upgrades.
- `npm view <pkg> dist-tags versions --json` - inspect release channels.

## Publish flow (safe order)
- `npm version patch|minor|major` - bump version and create tag.
- `npm pack` - inspect the tarball before publishing.
- `npm publish --access public` - first publish for scoped package.
- `npm deprecate <pkg>@<range> "message"` - warn users from old/bad versions.

## Version and release line
- Local check: `npm --version && node --version`
- Upstream release: `npm/cli` latest tag `v11.9.0` (2026-02-08 snapshot).
- Node LTS reference: `v24.13.0` ships npm `11.6.2`.

