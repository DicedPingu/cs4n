# Cargo — Rust’s build system and package manager
# Use it to build, test, and ship Rust crates and CLIs.

## 1) New project (ordered)
- `cargo new myapp` — new binary crate
- `cargo new --lib mylib` — new library crate
- `cd myapp`
- `cargo run` — build + run

## 2) Build / test / run
- `cargo build` — debug build
- `cargo build --release` — optimized build
- `cargo run` — run binary
- `cargo test` — run tests
- `cargo check` — fast type‑check only

## 3) Add / update deps
- `cargo add <crate>` — add dependency (needs cargo‑edit)
- `cargo add <crate> --features "feat1,feat2"` — enable features
- `cargo update` — update Cargo.lock
- `cargo update -p <crate>` — update one crate

## 4) Useful built‑ins
- `cargo fmt` — format (rustfmt)
- `cargo clippy` — lint (clippy)
- `cargo doc --open` — build + open docs
- `cargo bench` — benchmarks

## 5) Popular crates (what for)
- `serde` — serialization / deserialization
- `serde_json` — JSON support for serde
- `tokio` — async runtime
- `anyhow` — error handling (apps)
- `thiserror` — error enums (libs)
- `clap` — CLI arg parsing
- `reqwest` — HTTP client
- `tracing` + `tracing-subscriber` — structured logging
- `rayon` — data‑parallelism
- `parking_lot` — fast locks
- `dashmap` — concurrent hash map
- `sqlx` — async SQL

## 6) Cargo tools (install once)
- `cargo install cargo-edit` — enables `cargo add/rm/upgrade`
- `cargo install cargo-watch` — auto rebuild on change
- `cargo install cargo-nextest` — faster test runner
- `cargo install cargo-audit` — security advisory scan
- `cargo install cargo-deny` — licenses + bans
- `cargo install cargo-expand` — macro expansion view
- `cargo install cargo-udeps` — find unused deps
- `cargo install cargo-bloat` — binary size analysis
- `cargo install flamegraph` — CPU profiling
