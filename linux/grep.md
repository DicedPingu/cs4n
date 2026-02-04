# grep — search text
# Use it to find patterns in files.

- `grep "term" file` — basic search
- `grep -n "term" file` — line numbers
- `grep -i "term" file` — case‑insensitive
- `grep -r "term" .` — recursive
- `grep -E "a|b" file` — extended regex
- `grep -v "term" file` — invert match
- `grep -C 2 "term" file` — context lines
