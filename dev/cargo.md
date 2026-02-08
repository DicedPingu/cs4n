# Cargo - Rust build system and package manager
# Use it to build, test, lint, and publish Rust crates and applications.

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

