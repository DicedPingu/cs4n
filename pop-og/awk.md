# awk Quicksheet
Fast line-by-line text processing.

## core ideas
- `$0`, `$1`, `$2`...
  - What it does: `$0` is the whole line; `$1..$NF` are fields.
  - When to use it: Understanding how awk splits and targets data.
- `FS` and `OFS`
  - What it does: Input and output field separators.
  - When to use it: Working with CSV, TSV, or custom-delimited data.
- `NR`, `FNR`, `NF`
  - What it does: Total line number, file-local line number, and field count.
  - When to use it: Line-based logic and counting.

## common patterns
- `awk '{print $1}' file`
  - What it does: Prints the first field from each line.
  - When to use it: Extracting a column.
- `awk -F',' '{print $1,$3}' file`
  - What it does: Uses comma as the field separator and prints fields 1 and 3.
  - When to use it: CSV work without a full parser.
- `awk 'NR==1{print;next} {print $2,$1}' file`
  - What it does: Keeps header, then swaps column order on the rest.
  - When to use it: Quick column rearranges.
- `awk '$3 > 100 {print $1,$3}' file`
  - What it does: Filters rows where field 3 is greater than 100.
  - When to use it: Numeric filtering.
- `awk '/error|fail/ {print NR ":" $0}' file`
  - What it does: Prints matching lines with their line numbers.
  - When to use it: Quick log scanning.

## data shaping
- `awk '{sum+=$2} END{print sum}' file`
  - What it does: Sums column 2 and prints the total at the end.
  - When to use it: Lightweight aggregations.
- `awk 'BEGIN{print "col1","col2"} {print $1,$2} END{print NR " rows"}' file`
  - What it does: Adds a header and a footer count.
  - When to use it: Simple report formatting.
- `awk 'length($0) > 120' file`
  - What it does: Prints lines longer than 120 characters.
  - When to use it: Finding long lines in configs or code.
- `awk '{gsub(/foo/,"bar"); print}' file`
  - What it does: Replaces all occurrences of foo with bar on each line.
  - When to use it: Quick, streamed substitutions.
- `awk -v OFS='\t' '{print $1,$2,$3}' file`
  - What it does: Outputs tab-separated fields.
  - When to use it: Converting output for TSV tools.

## scripts
- `awk -f script.awk file`
  - What it does: Runs an awk script file.
  - When to use it: Reusing complex logic.
