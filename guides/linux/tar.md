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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `tar cf path/to/target.tar path/to/file1 path/to/file2 ...` | [c]reate an archive and write it to a [f]ile |
| `tar czf path/to/target.tar.gz path/to/file1 path/to/file2 ...` | [c]reate a g[z]ipped archive and write it to a [f]ile |
| `tar czf path/to/target.tar.gz [-C\|--directory] path/to/directory .` | [c]reate a g[z]ipped (compressed) archive from a directory using relative paths |
| `tar xvf path/to/source.tar[.gz\|.bz2\|.xz]` | E[x]tract a (compressed) archive [f]ile into the current directory [v]erbosely |
| `tar xf path/to/source.tar[.gz\|.bz2\|.xz] [-C\|--directory] path/to/directory` | E[x]tract a (compressed) archive [f]ile into the target directory |
| `tar caf path/to/target.tar.xz path/to/file1 path/to/file2 ...` | [c]reate a compressed archive and write it to a [f]ile, using the file extension to [a]utomatically determine the compression program |
| `tar tvf path/to/source.tar` | Lis[t] the contents of a tar [f]ile [v]erbosely |
| `tar xf path/to/source.tar --wildcards "*.html"` | E[x]tract files matching a pattern from an archive [f]ile |
| `tar --help` | Show command usage and option reference |
| `man tar` | Open the full manual page |
| `whatis tar` | Print one-line command description |
| `type -a tar` | Show how the shell resolves the command path |
| `command -v tar` | Print executable path used by current shell |
| `tldr tar` | Show concise command examples |
| `apropos tar` | Search manual database for related commands |
| `tar --version` | Print local tool version |
