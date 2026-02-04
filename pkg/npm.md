# npm — JavaScript/Node package manager
# Use it to install, update, run scripts, and publish packages.

## 1) Start a project
- `npm init -y` — create package.json fast
- `npm install <package>` — add dependency

## 2) Install
- `npm install` — install from package.json
- `npm ci` — clean, locked install (CI‑friendly)
- `npm install --omit=dev` — prod deps only
- `npm install --save-exact <pkg>` — exact version
- `npm install <pkg>@<ver>` — pin version
- `npm install <git_url>` — install from git

## 3) Add / remove
- `npm install <pkg>` — runtime dep
- `npm install -D <pkg>` — dev dep
- `npm uninstall <pkg>` — remove dep
- `npm uninstall -D <pkg>` — remove dev dep

## 4) Update + cleanup
- `npm outdated` — show updates
- `npm update` — update within semver
- `npm update <pkg>` — update one package
- `npm dedupe` — reduce duplicates
- `npm prune` — remove extraneous modules

## 5) Scripts
- `npm run` — list scripts
- `npm run <script>` — run script
- `npm run <script> -- <args>` — pass args
- `npm exec <cmd>` — run local CLI

## 6) Security
- `npm audit` — check vulnerabilities
- `npm audit fix` — auto‑fix
- `npm audit fix --force` — allow breaking fixes
- `npm audit -g` — not supported for globals

## 7) Global packages
- `npm install -g <pkg>` — install global CLI
- `npm update -g` — update globals
- `npm list -g --depth=0` — list globals
- `npm outdated -g --depth=0` — global updates

## 8) Publish
- `npm version patch|minor|major` — bump + tag
- `npm pack` — preview tarball
- `npm publish` — publish
- `npm publish --access public` — first scoped publish

## 9) Info + config
- `npm list --depth=0` — top‑level deps
- `npm view <pkg>` — package info
- `npm search <query>` — registry search
- `npm config get <key>` — read config
- `npm config set <key> <value>` — write config

## 10) Cache
- `npm cache verify` — check cache
- `npm cache clean --force` — wipe cache
