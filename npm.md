# npm (Practical Workflow Cheatsheet)

## 1) Start a new project (ordered)
1) `npm init -y`
2) `npm install <package>`
3) `npm run <script>`

## 2) Install dependencies (ordered)
- `npm install` — install from package.json
- `npm ci` — clean, locked install (best for CI)

## 3) Add / remove packages
- `npm install <package>`
- `npm install -D <package>`
- `npm install <package>@<version>`
- `npm install --save-exact <package>`
- `npm uninstall <package>`
- `npm uninstall -D <package>`

## 4) Update + cleanup
- `npm update`
- `npm update <package>`
- `npm outdated`
- `npm prune`
- `npm dedupe`

## 5) Scripts
- `npm run`
- `npm run <script>`
- `npm run <script> -- <args>`
- `npm test`
- `npm exec <command>`

## 6) Security
- `npm audit`
- `npm audit fix`

## 7) Global packages
- `npm install -g <package>`
- `npm update -g`
- `npm list -g --depth=0`
- `npm outdated -g --depth=0`
- `npm audit -g` — not supported (use project audits)

## 8) Versioning + publish
- `npm version patch | minor | major`
- `npm pack`
- `npm publish`
- `npm publish --access public`

## 9) Info + config
- `npm list --depth=0`
- `npm view <package>`
- `npm search <query>`
- `npm config get <key>`
- `npm config set <key> <value>`

## 10) Cache
- `npm cache verify`
- `npm cache clean --force`
