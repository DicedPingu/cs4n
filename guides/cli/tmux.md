# tmux - terminal multiplexer
Use it to keep shells alive across disconnects and organize parallel terminal work.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Session lifecycle
- `tmux new -s work` - create named session.
- `tmux ls` - list sessions.
- `tmux attach -t work` - attach session.
- `tmux kill-session -t work` - remove session.

## Window and pane control (prefix `Ctrl+b`)
- `c` - new window.
- `n` / `p` - next/previous window.
- `,` - rename window.
- `%` - split pane left/right.
- `"` - split pane top/bottom.
- `o` - cycle panes.
- `d` - detach session.

## Practical command-mode usage
- `tmux new -d -s ci 'make test'` - run detached job session.
- `tmux capture-pane -pt work:1 > pane.log` - export pane output.
- `tmux setw -g mouse on` - mouse support toggle.

## Recommended config snippets (`~/.tmux.conf`)
- `set -g history-limit 100000` - larger scrollback.
- `set -g renumber-windows on` - contiguous window numbering.
- `set -g set-clipboard on` - clipboard integration when supported.

## Version and release line
- Local check: `tmux -V`
- Upstream release snapshot: tmux `3.6a`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `tmux` | Start a new session |
| `tmux [new\|new-session] -s name` | Start a new named [s]ession |
| `tmux [ls\|list-sessions]` | List existing sessions |
| `tmux [a\|attach]` | Attach to the most recently used session |
| `<Ctrl b><d>` | Detach from the current session (inside a tmux session) |
| `<Ctrl b><c>` | Create a new window (inside a tmux session) |
| `<Ctrl b><w>` | Switch between sessions and windows (inside a tmux session) |
| `tmux kill-session -t name` | Kill a session by [t]arget name |
| `tmux --help` | Show command usage and option reference |
| `man tmux` | Open the full manual page |
| `whatis tmux` | Print one-line command description |
| `type -a tmux` | Show how the shell resolves the command path |
| `command -v tmux` | Print executable path used by current shell |
| `tldr tmux` | Show concise command examples |
| `apropos tmux` | Search manual database for related commands |
| `tmux --version` | Print local tool version |
