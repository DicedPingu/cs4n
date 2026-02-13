# cat - print and concatenate files
Use it for fast inspection or joining small text files.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Most common uses
- `cat file` - print file to stdout.
- `cat -n file` - show line numbers.
- `cat -A file` - show hidden characters and line endings.
- `cat a.txt b.txt > merged.txt` - concatenate files.

## Better options for large files
- `less file` - interactive paging (usually better than full `cat`).
- `tail -f app.log` - stream logs instead of dumping full file.
- `sed -n '1,60p' file` - inspect just the top section.

## Safer shell patterns
- `cat -- file-with-leading-dash` - avoid option confusion.
- `cat file | rg "term"` - quick pipe to search.

## Version and release line
- Local check: `cat --version`
- Upstream release snapshot: GNU coreutils `9.10`.

