# tar - create and extract archives
Use it to package directories for transfer, backup, or release artifacts.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Common archive flows
- `tar -czf out.tgz dir/` - create gzip-compressed tarball.
- `tar -xzf out.tgz` - extract gzip tarball.
- `tar -tf out.tgz` - list contents before extracting.
- `tar -C /dest -xzf out.tgz` - extract into specific directory.

## Precision options
- `tar --exclude='*.log' -czf out.tgz dir/` - exclude patterns.
- `tar -xzf out.tgz path/in/archive` - extract a single path.
- `tar --strip-components=1 -xzf out.tgz` - drop top directory during extraction.

## Compression variants
- `tar -cJf out.txz dir/` - xz compression (smaller, slower).
- `tar -cjf out.tbz2 dir/` - bzip2 compression.

## Version and release line
- Local check: `tar --version`
- Upstream release snapshot: GNU tar `1.35`.

