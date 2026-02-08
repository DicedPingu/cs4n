# xargs - build command arguments from stdin
# Use it to feed large input lists into commands efficiently.

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

