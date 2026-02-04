# Make — build automation for C/C++ and more
# Use it to build, test, install, and clean projects from a Makefile.

## 1) Build / update (ordered)
- `make` — build default target (usually `all`)
- `make -j$(nproc)` — parallel build (fast)
- `sudo make install` — install artifacts system‑wide
- `make install PREFIX=$HOME/.local` — install to user dir

## 2) Common targets (when defined)
- `make all` — full build
- `make test` — run tests
- `make check` — run checks (often same as test)
- `make bench` — benchmarks
- `make clean` — remove build outputs
- `make distclean` — deeper clean (removes config)
- `make uninstall` — remove installed files
- `make help` — list targets (if provided)

## 3) Useful options
- `make -n` — dry run (print commands)
- `make -k` — keep going after errors
- `make -C <dir>` — run in another directory
- `make -f <file>` — use a specific Makefile
- `make V=1` — verbose (if supported)

## 4) Override variables (common patterns)
- `make CC=clang` — use clang
- `make CXX=clang++` — use clang++
- `make CFLAGS="-O2 -g"` — compiler flags
- `make CXXFLAGS="-O2 -g"` — C++ flags
- `make LDFLAGS="-Wl,-rpath,$HOME/.local/lib"` — linker flags
- `make DESTDIR=/tmp/pkg install` — staging install
