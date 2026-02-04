# rg (ripgrep) — fast recursive search
# Use it to search codebases quickly.

## Basics
- `rg "term"` — search in current dir
- `rg "term" path/` — search in a path
- `rg -n "term"` — show line numbers

## Useful options
- `rg -i "term"` — case‑insensitive
- `rg -g "*.rs" "term"` — include glob
- `rg -g "!*.lock" "term"` — exclude glob
- `rg --hidden "term"` — include hidden files
- `rg -uu "term"` — include ignored + hidden
- `rg -F "literal"` — literal (no regex)
- `rg -C 3 "term"` — context lines
