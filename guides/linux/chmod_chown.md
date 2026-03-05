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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `chmod u+x path/to/file` | Give the [u]ser who owns a file the right to e[x]ecute it |
| `chmod u+rw path/to/file_or_directory` | Give the [u]ser rights to [r]ead and [w]rite to a file/directory |
| `chmod g-x path/to/file` | Remove e[x]ecutable rights from the [g]roup |
| `chmod a+rx path/to/file` | Give [a]ll users rights to [r]ead and e[x]ecute |
| `chmod o=g path/to/file` | Give [o]thers (not in the file owner's group) the same rights as the [g]roup |
| `chmod o= path/to/file` | Remove all rights from [o]thers |
| `chmod [-R\|--recursive] g+w,o+w path/to/directory` | Change permissions recursively giving [g]roup and [o]thers the ability to [w]rite |
| `chmod [-R\|--recursive] a+rX path/to/directory` | Recursively give [a]ll users [r]ead permissions to files. Also give e[X]ecute permissions to files that have at least one execution permission and to all sub-directories |
| `chmod --help` | Show command usage and option reference |
| `man chmod` | Open the full manual page |
| `whatis chmod` | Print one-line command description |
| `type -a chmod` | Show how the shell resolves the command path |
| `command -v chmod` | Print executable path used by current shell |
| `tldr chmod` | Show concise command examples |
| `apropos chmod` | Search manual database for related commands |
| `chmod --version` | Print local tool version |
| `sudo chown user path/to/file_or_directory` | Change the owner user of a file/directory |
| `sudo chown user:group path/to/file_or_directory` | Change the owner user and group of a file/directory |
| `sudo chown user: path/to/file_or_directory` | Change the owner user and group to both have the name `user` |
| `sudo chown [-R\|--recursive] user path/to/directory` | Recursively change the owner of a directory and its contents |
