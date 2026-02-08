# tmux - terminal multiplexer
# Use it to keep shells alive across disconnects and organize parallel terminal work.

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

