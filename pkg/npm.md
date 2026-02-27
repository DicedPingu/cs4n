# npm — Node.js package manager & script runner

Use npm for installing, versioning, publishing, and managing JavaScript/TypeScript dependencies. This expanded guide breaks down common workflows, offers 32+ useful commands, and groups them into categories for quick reference. Remember to run npm commands within your project directory (where `package.json` resides).

---

## Syntax & safety
- `<package>` = package name (e.g., `express`)
- `<version>` = semver specifier (e.g., `@^4.18.1`)
- `[flags]` = optional flags; most commands have short/long aliases
- Use `npm help <command>` or `npm <command> -h` for details
- When using global installs (`-g`), consider using `npx` or `pnpm` for a more isolated approach

---

## 0) Inspecting environment & configuration

| Command | Description |
| --- | --- |
| `npm --version` | show npm version |
| `node --version` | show Node.js version |
| `npm config list` | view current npm configuration |
| `npm config get <key>` | get a specific config value |
| `npm config set <key> <value>` | set config (writes to `.npmrc`) |
| `npm prefix -g` | show global install prefix |
| `npm doctor` | run diagnostic to detect common issues |
| `npm ls --depth=0` | list installed packages in current project |
| `npm outdated` | check for outdated dependencies |
| `npm audit` | run security audit on dependencies |
| `npm audit fix` | fix audit issues if safe |

---

## 1) Initializing and managing projects

| Command | Description |
| --- | --- |
| `npm init` | interactive creation of `package.json` |
| `npm init -y` | quick init with defaults |
| `npm init <@scope>/<pkg>` | initialize from a package template |
| `npm pkg set <key>=<value>` | modify `package.json` fields |
| `npm pkg get <key>` | read a field from `package.json` |
| `npm version <newversion>` | bump version and create git tag |
| `npm publish` | publish package to npm registry |
| `npm publish --access public` | publish scoped package publicly |
| `npm unpublish <pkg> --force` | remove published package (within 72h) |
| `npm pack` | create a `.tgz` tarball of package |

---

## 2) Installing & removing packages

### Local dependencies (project)

| Command | Description |
| --- | --- |
| `npm install <package>` | install and add to `dependencies` |
| `npm install <package>@<version>` | install specific version |
| `npm install <git repo>` | install from git URL |
| `npm install <folder>` | install from local folder |
| `npm install --save-dev <package>` | add to `devDependencies` |
| `npm install --save-peer <package>` | add to `peerDependencies` (npm ≥7) |
| `npm install --no-save <package>` | install without recording in `package.json` |
| `npm install --legacy-peer-deps` | ignore peer dependency conflicts (npm ≥7) |
| `npm install --ignore-scripts` | skip running `preinstall`/`install`/`postinstall` scripts |

### Global installs & tools

| Command | Description |
| --- | --- |
| `npm install -g <package>` | install globally |
| `npm update -g <package>` | update global package |
| `npm uninstall -g <package>` | remove global package |
| `npx <command>` | run the package without installing globally |
| `npm list -g --depth=0` | list globally installed packages |

### Removing / cleaning

| Command | Description |
| --- | --- |
| `npm uninstall <package>` | remove dependency and update `package.json` |
| `npm prune` | remove extraneous packages not in `package.json` |
| `npm dedupe` | de-duplicate packages in node_modules |
| `npm cache verify` | verify contents of npm cache |
| `npm cache clean --force` | clear npm cache |

---

## 3) Updating & version management

| Command | Description |
| --- | --- |
| `npm update` | update all dependencies to semver-compatible versions |
| `npm update <package>` | update specific package |
| `npm outdated` | show outdated dependencies with available versions |
| `npm view <package> versions` | list all versions of a package |
| `npm view <package> version` | show latest version |
| `npm install <package>@latest` | install latest version |
| `npm install <package>@next` | install next/prerelease version |
| `npm ci` | clean install from `package-lock.json` (ideal for CI) |
| `npm rebuild` | rebuild any compiled modules |

---

## 4) Scripts & automation

| Command | Description |
| --- | --- |
| `npm run <script>` | run script defined in `package.json` |
| `npm run` | list available scripts |
| `npm test` | alias for `npm run test` |
| `npm start` | alias for `npm run start` |
| `npm stop` | alias for `npm run stop` |
| `npm restart` | run `stop` then `start` script |
| `npm run <script> -- <args>` | pass arguments to script |
| `npm exec <command>` | run package binary in PATH without script |
| `npm set-script <name> "<cmd>"` | add or update script in `package.json` |

---

## 5) Package-lock, workspaces, & audit

| Command | Description |
| --- | --- |
| `npm install` | respect `package-lock.json` and install exact versions |
| `npm ci` | remove existing `node_modules` and reinstall as per lockfile |
| `npm shrinkwrap` | generate `npm-shrinkwrap.json` (lockfile for packages intended for publish) |
| `npm audit` | run security audit |
| `npm audit fix` | attempt to automatically fix vulnerabilities |
| `npm workspaces list` | list configured workspaces |
| `npm install <pkg> -w <workspace>` | install package in a specific workspace |
| `npm run <script> -w <workspace>` | run script in workspace |

---

## 6) Registries & proxies

| Command | Description |
| --- | --- |
| `npm config set registry <url>` | set default registry |
| `npm config delete registry` | revert to npmjs.org |
| `npm login` | authenticate with registry |
| `npm logout` | remove registry auth token |
| `npm whoami` | print username for current registry |
| `npm search <term>` | search registry for packages |
| `npm config set proxy http://proxy:port` | configure HTTP proxy |
| `npm config set https-proxy http://proxy:port` | configure HTTPS proxy |
| `npm config set strict-ssl false` | disable SSL verification (not recommended) |

---

## 7) Miscellaneous & diagnostics

| Command | Description |
| --- | --- |
| `npm explain <package>` | explain why a package is installed and by whom |
| `npm fund` | show funding links for dependencies |
| `npm help <command>` | view detailed help for any npm subcommand |
| `npm docs <package>` | open package’s documentation in browser |
| `npm view <package>` | fetch package metadata |
| `npm org set <@scope>:<key>=<value>` | set organization-level configs |
| `npm profile get` | show user profile info |
| `npm hook add <pkg> <event> <url>` | add web hook for package events |
| `npm ping <registry>` | test registry connectivity |
| `npm rebuild <package>` | rebuild a specific installed package |
| `npm link` | symlink global package to local node_modules for development |
| `npm unlink` | remove symlink created by link |

---

## Resources & docs

- Official docs: https://docs.npmjs.com/
- For single-run commands without global installs, use `npx` (ships with npm ≥5.2)
