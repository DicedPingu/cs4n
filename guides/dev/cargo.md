# Cargo - Rust build system and package manager
Use it to build, test, lint, and publish Rust crates and applications.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Standard development loop
- `cargo check` - fast type and borrow checks.
- `cargo test` - run tests.
- `cargo clippy --all-targets --all-features -- -D warnings` - strict linting.
- `cargo fmt --check` - formatting gate.
- `cargo run` - run current binary target.

## Dependency and feature management
- `cargo add <crate>` - add dependency (via cargo-edit).
- `cargo add <crate> --features "feat1,feat2"` - enable crate features.
- `cargo update -p <crate>` - upgrade one lockfile dependency.
- `cargo tree -i <crate>` - reverse dependency tree.

## Build profiles and artifacts
- `cargo build` - debug build.
- `cargo build --release` - optimized release build.
- `cargo doc --no-deps --open` - build local docs.
- `cargo bench` - benchmark target run.

## Publish and workspace hygiene
- `cargo package --allow-dirty` - inspect package archive before publish.
- `cargo publish --dry-run` - registry validation pass.
- `cargo publish` - push crate to crates.io.

## Common companion tools
- `cargo install cargo-nextest` - faster test execution.
- `cargo install cargo-audit` - security advisory scanning.
- `cargo install cargo-deny` - policy checks (licenses/advisories).

## Version and release line
- Local check: `cargo --version && rustc --version`
- Stable release snapshot: Rust/Cargo `1.93.0` toolchain line.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `cargo search search_string` | Search for crates |
| `cargo install crate_name` | Install a binary crate |
| `cargo install --list` | List installed binary crates |
| `cargo init --bin\|lib path/to/directory` | Create a new binary or library Rust project in the specified directory (or the current working directory by default) |
| `cargo add dependency` | Add a dependency to `Cargo.toml` in the current directory |
| `cargo [b\|build] [-r\|--release]` | Build the Rust project in the current directory using the release profile |
| `cargo +nightly [b\|build]` | Build the Rust project in the current directory using the nightly compiler (requires `rustup`) |
| `cargo [b\|build] --jobs number_of_threads` | Build using a specific number of threads (default is the number of logical CPUs) |
| `cargo --help` | Show command usage and option reference |
| `man cargo` | Open the full manual page |
| `whatis cargo` | Print one-line command description |
| `type -a cargo` | Show how the shell resolves the command path |
| `command -v cargo` | Print executable path used by current shell |
| `tldr cargo` | Show concise command examples |
| `apropos cargo` | Search manual database for related commands |
| `cargo --version` | Print local tool version |
