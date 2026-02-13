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

