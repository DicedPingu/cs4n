# grep - pattern search in text
# Use it for fast filtering in files, logs, and pipelines.

## Core usage
- `grep "term" file` - basic search.
- `grep -n "term" file` - include line numbers.
- `grep -i "term" file` - case-insensitive search.
- `grep -r "term" .` - recursive directory search.

## Better matching control
- `grep -E "warn|error" file` - extended regex.
- `grep -F "literal.text" file` - fixed-string mode.
- `grep -v "term" file` - invert match.
- `grep -C 2 "term" file` - show surrounding context.

## Typical pairings
- `journalctl -u app | grep -i error` - service error stream.
- `ps aux | grep '[n]ginx'` - avoid matching the grep process line.

## Version and release line
- Local check: `grep --version`
- Upstream release snapshot: GNU grep `3.12`.

