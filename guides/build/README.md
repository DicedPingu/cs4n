# Build Guides
Deterministic local build workflows and artifact generation.

## Files and locations
- `guides/build/cmake.md` - configure/build/test/install with CMake.
- `guides/build/make.md` - classic Makefile flows and options.

## Recommended order
1. `cmake.md` for CMake projects.
2. `make.md` for Makefile-first projects.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `cmake -S . -B build` | Configure out-of-source build directory |
| `cmake -S . -B build -D CMAKE_BUILD_TYPE=Release` | Configure release profile |
| `cmake --build build -j"$(nproc)"` | Build with parallel jobs |
| `ctest --test-dir build --output-on-failure` | Run tests and print failing test output |
| `cmake --install build --prefix ~/.local` | Install artifacts into custom prefix |
| `cmake -S . -B build -G Ninja` | Generate Ninja build files |
| `cmake --build build --target clean` | Clean via generated build system |
| `make -n` | Dry-run to inspect what make would execute |
| `make -j"$(nproc)"` | Parallel build with all CPU cores |
| `make V=1` | Show full compile/link commands |
| `make test` | Run project test target if defined |
| `make install DESTDIR=/tmp/pkgroot` | Stage install files into packaging root |
