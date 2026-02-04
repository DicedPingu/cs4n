# sed Quicksheet
Stream edits and transforms.

## basics
- `sed 's/foo/bar/' file`
  - What it does: Replaces the first foo per line with bar.
  - When to use it: Simple substitutions.
- `sed 's/foo/bar/g' file`
  - What it does: Replaces all foo matches per line.
  - When to use it: Global replacements.
- `sed -n '1,5p' file`
  - What it does: Prints lines 1 through 5.
  - When to use it: Quick range preview.
- `sed '/pattern/d' file`
  - What it does: Deletes lines that match pattern.
  - When to use it: Filtering out noise.

## common edits
- `sed -E 's/([0-9]+)px/\1rem/g' file`
  - What it does: Uses extended regex to convert px to rem.
  - When to use it: Bulk CSS conversions.
- `sed 's/[[:space:]]\+$//' file`
  - What it does: Removes trailing whitespace.
  - When to use it: Cleaning files before commit.
- `sed 's/^/# /' file`
  - What it does: Prefixes each line.
  - When to use it: Commenting blocks or markdown.
- `sed -n '/error/p' file`
  - What it does: Prints only lines that match error.
  - When to use it: Log scanning without grep.
- `sed '3,7d' file`
  - What it does: Deletes lines 3 through 7.
  - When to use it: Removing a block of lines.

## in-place editing
- `sed -i 's/foo/bar/g' file`
  - What it does: Edits the file in place.
  - When to use it: Confident replacements.
- `sed -i.bak 's/foo/bar/g' file`
  - What it does: Edits in place and keeps a backup.
  - When to use it: Safer batch edits.
- `sed -e 's/a/b/' -e 's/c/d/' file`
  - What it does: Runs multiple expressions in one command.
  - When to use it: Stacking small transforms.

## scripts
- `sed -f script.sed file`
  - What it does: Runs a sed script file.
  - When to use it: Reusable or complex edits.
