# cat Quicksheet
View and concatenate files.

## basics
- `cat file`
  - What it does: Prints file contents to stdout.
  - When to use it: Quick file peek or piping.
- `cat file1 file2 > combined.txt`
  - What it does: Concatenates multiple files into one.
  - When to use it: Merging logs or configs.
- `cat > file.txt`
  - What it does: Creates or overwrites a file from stdin.
  - When to use it: Quick file creation without an editor.
- `cat >> file.txt`
  - What it does: Appends stdin to a file.
  - When to use it: Adding lines or blocks to a file.

## useful flags
- `cat -n file`
  - What it does: Numbers all lines.
  - When to use it: Referencing specific lines.
- `cat -b file`
  - What it does: Numbers non-empty lines only.
  - When to use it: Scripts or docs where blanks are noise.
- `cat -A file`
  - What it does: Shows non-printing characters and line endings.
  - When to use it: Debugging whitespace or formatting issues.
- `cat -s file`
  - What it does: Squeezes multiple blank lines into one.
  - When to use it: Cleaning up noisy output.
- `cat -E file`
  - What it does: Shows `$` at end of each line.
  - When to use it: Visualizing trailing spaces and line breaks.

## patterns
- `cat /etc/os-release`
  - What it does: Prints distro info.
  - When to use it: Quick system identification.
- `cat file | less`
  - What it does: Pipes output to a pager.
  - When to use it: Long files you want to scroll.
- `cat file | wc -l`
  - What it does: Counts lines.
  - When to use it: Quick line totals.
