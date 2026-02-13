# CMake - cross-platform build generator
Use it to configure, build, test, and install C/C++ projects in a reproducible way.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Recommended out-of-source workflow
- `cmake -S . -B build -G Ninja` - configure with Ninja generator.
- `cmake --build build -j$(nproc)` - parallel build.
- `ctest --test-dir build --output-on-failure` - run tests.
- `cmake --install build` - install artifacts.

## Common configure options
- `-DCMAKE_BUILD_TYPE=Debug|Release|RelWithDebInfo` - build profile.
- `-DCMAKE_EXPORT_COMPILE_COMMANDS=ON` - enable `compile_commands.json` for clangd.
- `-DCMAKE_INSTALL_PREFIX=$HOME/.local` - user-space install.
- `-DCMAKE_PREFIX_PATH=/path/to/deps` - locate external dependencies.

## Targeted builds and diagnostics
- `cmake --build build --target <name>` - build one target.
- `cmake -LAH -S . -B build` - inspect cached variables.
- `cmake --fresh -S . -B build` - reconfigure from clean cache.

## Cleanup strategy
- `cmake --build build --target clean` - project-defined clean.
- `rm -rf build` - full reset when cache is inconsistent.

## Version and release line
- Local check: `cmake --version`
- Upstream release snapshot: CMake `v4.2.3`.

