# Make (GNU Make) (Practical Workflow Cheatsheet)

## 1) Build / update (ordered)
- `make`
- `make -j$(nproc)`
- `sudo make install`

## 2) Clean / test
- `make clean`
- `make test`

## 3) Useful options
- `make -n` (dry‑run)
- `make -C <dir>` (run in another dir)
- `make -f <file>` (use a specific Makefile)
- `make -k` (keep going on errors)
- `make V=1` or `make VERBOSE=1` (if supported)
- `make CC=clang CFLAGS="-O2 -g"`

## 4) Misc
- `.PHONY: <target>`
