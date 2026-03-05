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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `npm init [-y\|--yes]` | Create a `package.json` file with default values (omit `--yes` to do it interactively) |
| `npm [i\|install]` | Download all the packages listed as dependencies in `package.json` |
| `npm [i\|install] package_name@version` | Download a specific version of a package and add it to the list of dependencies in `package.json` |
| `npm [i\|install] package_name [-D\|--save-dev]` | Download the latest version of a package and add it to the list of dev dependencies in `package.json` |
| `npm [i\|install] package_name [-g\|--global]` | Download the latest version of a package and install it globally |
| `npm [r\|uninstall] package_name` | Uninstall a package and remove it from the list of dependencies in `package.json` |
| `npm [ls\|list]` | List all locally installed dependencies |
| `npm [ls\|list] [-g\|--global] --depth 0` | List all top-level globally installed packages |
| `npm --help` | Show command usage and option reference |
| `man npm` | Open the full manual page |
| `whatis npm` | Print one-line command description |
| `type -a npm` | Show how the shell resolves the command path |
| `command -v npm` | Print executable path used by current shell |
| `tldr npm` | Show concise command examples |
| `apropos npm` | Search manual database for related commands |
| `npm --version` | Print local tool version |
| `tldr npm exec` | View documentation for the original command |
| `npx --help` | Show command usage and option reference |
| `man npx` | Open the full manual page |
| `whatis npx` | Print one-line command description |
