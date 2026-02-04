# htop

`htop` is an interactive system-monitor process viewer and process manager. It offers a more user-friendly and colorful alternative to the classic `top` command.

## Installation

If not installed by default:

```bash
sudo apt install htop  # Debian/Ubuntu/Pop!_OS
```

## Basic Usage

Simply run `htop` in the terminal:

```bash
htop
```

## Interface Overview

- **Top Section**: Shows CPU usage bars (one per core), Memory/Swap usage, and system Uptime/Load Average.
- **Main Area**: A list of running processes.
- **Bottom Bar**: Function keys for common actions.

## Key Shortcuts

- **F2 (Setup)**: Customize the display (colors, columns, meters).
- **F3 (Search)**: Search for a running process by name.
- **F4 (Filter)**: Filter the process list (very useful to find specific PIDs).
- **F5 (Tree)**: Toggle tree view to see process parent-child relationships.
- **F6 (Sort)**: Select a column to sort by (e.g., CPU%, MEM%).
- **F9 (Kill)**: Send a signal to the selected process (e.g., SIGTERM, SIGKILL).
- **F10 (Quit)**: Exit htop.

## Mouse Support

`htop` supports mouse interaction. You can click column headers to sort, or click processes to select/kill them.
