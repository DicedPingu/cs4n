# npm publish - package release workflow
Use it when releasing JavaScript/TypeScript packages to npm safely.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Pre-publish validation (required)
- `npm ci` - clean lockfile install.
- `npm test` - run tests before release.
- `npm run build` - create publishable build artifacts.
- `npm pack --dry-run` - preview exactly what will be published.

## Versioning and tags
- `npm version patch|minor|major` - bump version and create git tag.
- `npm version prerelease --preid rc` - create release candidate versions.
- `git push --follow-tags` - push commits and version tags together.

## Publish commands
- `npm publish` - publish to npm using package visibility defaults.
- `npm publish --access public` - required first publish for scoped public packages.
- `npm publish --tag next` - publish to a non-default dist-tag (e.g., pre-release channel).

## Post-publish checks and rollback strategy
- `npm view <pkg> dist-tags versions --json` - verify published version and tags.
- `npm deprecate <pkg>@<range> "message"` - mark bad versions with migration guidance.
- `npm unpublish <pkg>@<version>` - remove version (only if npm policy/time window allows).

## Version and release line
- Local check: `npm --version && node --version`
- Snapshot line: npm `11.9.0`, Node LTS `24.13.0`.
- Upstream source: `npm/cli` latest release and Node release index.
