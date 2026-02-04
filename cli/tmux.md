# tmux — terminal multiplexer
# Use it to keep sessions alive and split panes.

## Basics
- `tmux` — start session
- `tmux new -s name` — named session
- `tmux ls` — list sessions
- `tmux attach -t name` — attach session
- `tmux kill-session -t name` — kill session

## Common keys (prefix = Ctrl+b)
- `c` — new window
- `n` / `p` — next/prev window
- `"` — split vertically
- `%` — split horizontally
- `o` — next pane
- `d` — detach

## Quality of life
- `tmux rename-session name` — rename
- `tmux rename-window name` — rename window
