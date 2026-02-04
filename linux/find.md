# find — locate files and run actions
# Use it for search + batch operations.

- `find . -name "*.log"` — by name
- `find . -type f` — files only
- `find . -mtime -1` — modified in last day
- `find . -maxdepth 2 -name "*.md"` — limit depth
- `find . -name "*.tmp" -delete` — delete matches
- `find . -name "*.py" -exec rg "TODO" {} \;` — exec per file
