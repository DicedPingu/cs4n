# xargs — build command lines from stdin
# Use it to apply commands to lists.

- `cat files.txt | xargs rm` — delete listed files
- `find . -print0 | xargs -0 rm` — safe with spaces
- `printf '%s\n' a b | xargs -I{} echo {}.log` — template
- `xargs -n 1 cmd` — one arg per command
