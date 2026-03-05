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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `cmake path/to/project_directory` | Generate a build recipe in the current directory with `CMakeLists.txt` from a project directory |
| `cmake --build path/to/build_directory` | Use a generated recipe in a given directory to build artifacts |
| `cmake --install path/to/build_directory --strip` | Install the build artifacts into `/usr/local/` and strip debugging symbols |
| `cmake path/to/project_directory -D CMAKE_BUILD_TYPE=Release` | Generate a build recipe, with build type set to `Release` with CMake variable |
| `cmake -G generator_name path/to/project_directory` | Generate a build recipe using `generator_name` as the underlying build system |
| `cmake --install path/to/build_directory --strip --prefix path/to/directory` | Install the build artifacts using a custom prefix for paths |
| `cmake --build path/to/build_directory [-t\|--target] target_name` | Run a custom build target |
| `cmake [-h\|--help]` | Display help |
| `cmake --help` | Show command usage and option reference |
| `man cmake` | Open the full manual page |
| `whatis cmake` | Print one-line command description |
| `type -a cmake` | Show how the shell resolves the command path |
| `command -v cmake` | Print executable path used by current shell |
| `tldr cmake` | Show concise command examples |
| `apropos cmake` | Search manual database for related commands |
| `cmake --version` | Print local tool version |
