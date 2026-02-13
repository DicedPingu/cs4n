# Make - build automation from Makefiles
Use it for deterministic build/test/install targets in C/C++ and mixed projects.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Common project loop
- `make -j$(nproc)` - parallel default target build.
- `make test` - run tests if target exists.
- `make install PREFIX=$HOME/.local` - user-space install.
- `make clean` - clear generated outputs.

## Useful control flags
- `make -n` - dry run (show commands without executing).
- `make -k` - keep going after errors.
- `make V=1` - verbose toolchain output (if Makefile supports it).
- `make -C <dir>` - run using another working directory.

## Variable override examples
- `make CC=clang CXX=clang++` - switch compiler.
- `make CFLAGS='-O2 -g'` - C flags.
- `make CXXFLAGS='-O2 -g'` - C++ flags.
- `make DESTDIR=/tmp/pkg install` - staging install root for packaging.

## Target discovery
- `make help` - project help target (if present).
- `make -qp | rg '^[a-zA-Z0-9_.-]+:'` - inspect parsed targets quickly.

## Version and release line
- Local check: `make --version`
- Upstream release snapshot: GNU Make `4.4.1`.

