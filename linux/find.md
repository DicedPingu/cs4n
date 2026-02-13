# find - recursive file search and action runner
Use it to locate files by name/type/time and perform batch actions safely.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## High-value searches
- `find . -type f -name "*.log"` - find log files.
- `find . -type d -name "node_modules"` - find directories.
- `find . -mtime -1` - modified in last 24 hours.
- `find . -maxdepth 2 -name "*.md"` - limit recursion depth.

## Safer batch actions
- `find . -name "*.tmp" -print` - inspect first.
- `find . -name "*.tmp" -delete` - delete matches after confirming.
- `find . -type f -name "*.py" -exec rg -n "TODO" {} +` - pass many files per exec.

## Space-safe piping
- `find . -type f -print0 | xargs -0 rm` - robust with spaces/newlines.
- `find . -type f -print0 | xargs -0 -n1 basename` - transform file list safely.

## Version and release line
- Local check: `find --version`
- Upstream release snapshot: GNU findutils `4.10.0`.

