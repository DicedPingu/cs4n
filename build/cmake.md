# CMake — cross‑platform build generator
# Use it to configure and build C/C++ projects.

## 1) Configure / build (recommended)
- `cmake -S . -B build` — configure into build/ dir
- `cmake --build build -j$(nproc)` — build
- `cmake --install build` — install (if defined)

## 2) Common options
- `-DCMAKE_BUILD_TYPE=Release` — optimized build
- `-DCMAKE_PREFIX_PATH=...` — find custom deps
- `-G Ninja` — use Ninja generator
- `-DCMAKE_EXPORT_COMPILE_COMMANDS=ON` — clangd support
- `-DCMAKE_INSTALL_PREFIX=$HOME/.local` — user install

## 3) Targets / introspection
- `cmake --build build --target <name>` — build target
- `cmake -LAH -S . -B build` — show cache values
- `ctest --test-dir build` — run tests (if configured)

## 4) Cleanup
- `rm -rf build` — full clean
