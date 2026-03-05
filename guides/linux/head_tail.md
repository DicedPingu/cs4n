# head / tail - view beginning or end of files
Use them for quick sampling and live log monitoring.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily use
- `head -n 30 file` - first lines.
- `tail -n 30 file` - last lines.
- `tail -f app.log` - follow appended lines.
- `tail -F app.log` - follow across log rotation.

## Precision patterns
- `head -c 200 file.bin` - first N bytes.
- `tail -c 200 file.bin` - last N bytes.
- `tail -n +50 file` - start from line 50.

## Good combinations
- `tail -f app.log | grep -i error` - live error filter.
- `head -n 1 file && tail -n 1 file` - check boundaries quickly.

## Version and release line
- Local check: `head --version && tail --version`
- Upstream release snapshot: GNU coreutils `9.10`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `head -n count path/to/file` | Output the first few lines of a file |
| `head --help` | Show command usage and option reference |
| `man head` | Open the full manual page |
| `whatis head` | Print one-line command description |
| `type -a head` | Show how the shell resolves the command path |
| `command -v head` | Print executable path used by current shell |
| `tldr head` | Show concise command examples |
| `apropos head` | Search manual database for related commands |
| `head --version` | Print local tool version |
| `tail path/to/file` | Show last 10 lines in a file |
| `tail path/to/file1 path/to/file2 ...` | Show last 10 lines of multiple files |
| `tail [-n\|--lines] count path/to/file` | Show last `count` lines in file |
| `tail [-n\|--lines] +count path/to/file` | Print a file from a specific line number |
| `tail [-c\|--bytes] count path/to/file` | Print a specific count of bytes from the end of a given file |
| `tail [-f\|--follow] path/to/file` | Print the last lines of a given file and keep reading it until `<Ctrl c>` |
| `tail [-F\|--retry --follow] path/to/file` | Keep reading file until `<Ctrl c>`, even if the file is inaccessible |
| `tail [-n\|--lines] count [-s\|--sleep-interval] seconds [-f\|--follow] path/to/file` | Show last `count` lines in a file and refresh every `seconds` seconds |
| `tail --help` | Show command usage and option reference |
| `man tail` | Open the full manual page |
| `whatis tail` | Print one-line command description |
