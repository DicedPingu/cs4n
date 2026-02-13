# chmod / chown - permissions and ownership
Use them to control who can read, write, or execute files and directories.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Permission model quick map
- `r` read, `w` write, `x` execute.
- Triplets apply to `user`, `group`, `others`.

## Common chmod patterns
- `chmod 644 file` - owner read/write, others read.
- `chmod 755 dir_or_script` - executable by all, writable by owner.
- `chmod +x script.sh` - add execute bit.
- `chmod -R u=rwX,go=rX dir/` - safe recursive defaults.

## Common chown patterns
- `chown user:group file` - set owner and group.
- `chown -R user:group dir/` - recursive ownership.
- `chown :group file` - change group only.

## Safety notes
- Use `ls -l` before and after mass changes.
- Avoid `chmod -R 777`; use targeted write permissions instead.

## Version and release line
- Local check: `chmod --version && chown --version`
- Upstream release snapshot: GNU coreutils `9.10`.

