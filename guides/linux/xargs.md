# xargs - build command arguments from stdin
Use it to feed large input lists into commands efficiently.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Core patterns
- `printf '%s\n' a b c | xargs -n1 echo` - one argument per command call.
- `cat files.txt | xargs rm` - apply command to listed paths.
- `find . -type f -print0 | xargs -0 rm` - robust with spaces/newlines.

## Template and parallel execution
- `printf '%s\n' app db cache | xargs -I{} echo deploy-{}` - placeholder template.
- `xargs -P 4 -n1 < jobs.txt ./run-task` - parallel worker execution.

## Safety practices
- Prefer `-0` with `find -print0` for filesystem paths.
- Use `echo` as dry run first, then swap to destructive command.

## Version and release line
- Local check: `xargs --version`
- Upstream release snapshot: GNU findutils `4.10.0`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `arguments_source \| xargs command` | Run a command using the input data as arguments |
| `arguments_source \| xargs sh -c "command1 && command2 \| command3"` | Run multiple chained commands on the input data |
| `find . -name '*.log' -print0 \| xargs [-0\|--null] [-P\|--max-procs] 4 [-n\|--max-args] 1 gzip` | Gzip all files with `.log` extension taking advantage of multiple threads (`-print0` uses a null character to split file names, and `-0` uses it as delimiter) |
| `arguments_source \| xargs [-n\|--max-args] 1 command` | Execute the command once per argument |
| `arguments_source \| xargs -I _ command _ optional_extra_arguments` | Execute the command once for each input line, replacing any occurrences of the placeholder (here marked as `_`) with the input line |
| `arguments_source \| xargs [-P\|--max-procs] max-procs command` | Parallel runs of up to `max-procs` processes at a time; the default is 1. If `max-procs` is 0, xargs will run as many processes as possible at a time |
| `arguments_source \| xargs [-p\|--interactive] command` | Prompt user for confirmation before executing command (confirm with `y` or `Y`) |
| `xargs --help` | Show command usage and option reference |
| `man xargs` | Open the full manual page |
| `whatis xargs` | Print one-line command description |
| `type -a xargs` | Show how the shell resolves the command path |
| `command -v xargs` | Print executable path used by current shell |
| `tldr xargs` | Show concise command examples |
| `apropos xargs` | Search manual database for related commands |
| `xargs --version` | Print local tool version |
