# sed — stream editor
# Use it for quick find/replace and filtering.

- `sed -n '1,5p' file` — print lines 1–5
- `sed 's/old/new/' file` — replace first match per line
- `sed 's/old/new/g' file` — replace all matches
- `sed -i 's/old/new/g' file` — in‑place edit
- `sed '/^#/d' file` — delete comment lines
