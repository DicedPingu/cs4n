# chmod / chown - permissions and ownership
# Use them to control who can read, write, or execute files and directories.

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

