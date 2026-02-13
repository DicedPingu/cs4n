# Build Guides
Use these when you need deterministic local builds and installable artifacts.

## Start order
1. `cmake.md` for CMake-based projects (most modern C/C++ repos).
2. `make.md` for classic Makefile workflows.

## Practical rule
- Always run a dry or inspect command first (`cmake -LAH ...`, `make -n`) before destructive cleanup.
