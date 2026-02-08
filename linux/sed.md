# sed - stream editor for text transforms
# Use it for line filtering and in-place replacements.

## Fast patterns
- `sed -n '1,20p' file` - print line range.
- `sed 's/old/new/' file` - replace first match per line.
- `sed 's/old/new/g' file` - replace all matches per line.
- `sed '/^#/d' file` - drop comment lines.

## In-place edits (careful)
- `sed -i 's/old/new/g' file` - edit file directly.
- `sed -i.bak 's/old/new/g' file` - keep backup copy.

## Multi-step transforms
- `sed -e 's/foo/bar/g' -e '/^$/d' file` - chain expressions.
- `rg -l 'old' . | xargs sed -i 's/old/new/g'` - repo-wide replacement (review first).

## Version and release line
- Local check: `sed --version`
- Upstream release snapshot: GNU sed `4.9`.

