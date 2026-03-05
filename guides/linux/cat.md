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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `cat path/to/file` | Print the contents of a file to `stdout` |
| `cat path/to/file1 path/to/file2 ... > path/to/output_file` | Concatenate several files into an output file |
| `cat path/to/file1 path/to/file2 ... >> path/to/output_file` | Append several files to an output file |
| `cat -u /dev/tty12 > /dev/tty13` | Copy the contents of a file into an output file without buffering |
| `cat - > path/to/file` | Write `stdin` to a file |
| `cat --help` | Show command usage and option reference |
| `man cat` | Open the full manual page |
| `whatis cat` | Print one-line command description |
| `type -a cat` | Show how the shell resolves the command path |
| `command -v cat` | Print executable path used by current shell |
| `tldr cat` | Show concise command examples |
| `apropos cat` | Search manual database for related commands |
| `cat --version` | Print local tool version |
