# tar Quicksheet
Create and extract archives.

## create archives
- `tar -cf archive.tar dir/`
  - What it does: Creates a tar archive.
  - When to use it: Bundling files without compression.
- `tar -czf archive.tar.gz dir/`
  - What it does: Creates a gzip-compressed tarball.
  - When to use it: Smaller archives for transfer.
- `tar -cJf archive.tar.xz dir/`
  - What it does: Creates an xz-compressed tarball.
  - When to use it: Maximum compression.

## extract archives
- `tar -xf archive.tar`
  - What it does: Extracts a tar archive.
  - When to use it: Unpacking local archives.
- `tar -xzf archive.tar.gz`
  - What it does: Extracts a gzip tarball.
  - When to use it: Most common downloads.
- `tar -xJf archive.tar.xz`
  - What it does: Extracts an xz tarball.
  - When to use it: Smaller, slower extractions.

## inspect
- `tar -tf archive.tar.gz`
  - What it does: Lists contents without extracting.
  - When to use it: Checking what’s inside.
- `tar -xzf archive.tar.gz -C /tmp/out`
  - What it does: Extracts to a target directory.
  - When to use it: Keep unpacking tidy.
