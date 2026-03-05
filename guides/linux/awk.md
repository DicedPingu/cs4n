# awk - field-oriented text processing
Use it to extract columns, filter rows, and aggregate values from structured text.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily patterns
- `awk '{print $1}' file` - print first column.
- `awk -F, '{print $1,$3}' file.csv` - parse comma-separated fields.
- `awk 'NR==1{print; next} $3 > 10' file` - keep header and filter rows.
- `awk '{sum += $3} END {print sum}' file` - sum numeric column.

## Slightly advanced
- `awk 'BEGIN{OFS=","} {print $1,$2}' file` - set output separator.
- `awk '$2 ~ /error|warn/i' file` - regex match in a specific field.
- `awk 'length($0) > 120' file` - filter long lines.

## Pair with other commands
- `rg "pattern" file | awk '{print $1}'` - filter then select fields.
- `journalctl -u app -n 200 | awk '/ERROR/ {print $0}'` - narrow log output.

## Version and release line
- Local check: `awk --version`
- Upstream release snapshot: GNU awk (gawk) `5.3.2`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `awk '{print $5}' path/to/file` | Print the fifth column (a.k.a. field) in a space-separated file |
| `awk '/foo/ {print $2}' path/to/file` | Print the second column of the lines containing "foo" in a space-separated file |
| `awk -F ',' '{print $NF}' path/to/file` | Print the last column of each line in a file, using a comma (instead of space) as a field separator |
| `awk '{s+=$1} END {print s}' path/to/file` | Sum the values in the first column of a file and print the total |
| `awk 'NR%3==1' path/to/file` | Print every third line starting from the first line |
| `awk '{if ($1 == "foo") print "Exact match foo"; else if ($1 ~ "bar") print "Partial match bar"; else print "Baz"}' path/to/file` | Print different values based on conditions |
| `awk '($10 >= min_value && $10 <= max_value)'` | Print all the lines which the 10th column value is between a min and a max |
| `awk 'BEGIN {FS=":";printf "%-20s %6s %25s\n", "Name", "UID", "Shell"} $4 >= 1000 {printf "%-20s %6d %25s\n", $1, $4, $7}' /etc/passwd` | Print table of users with UID >=1000 with header and formatted output, using colon as separator (`%-20s` mean: 20 left-align string characters, `%6s` means: 6 right-align string characters) |
| `awk --help` | Show command usage and option reference |
| `man awk` | Open the full manual page |
| `whatis awk` | Print one-line command description |
| `type -a awk` | Show how the shell resolves the command path |
| `command -v awk` | Print executable path used by current shell |
| `tldr awk` | Show concise command examples |
| `apropos awk` | Search manual database for related commands |
| `awk --version` | Print local tool version |
