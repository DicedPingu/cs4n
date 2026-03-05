# Dev Guides
Language and framework workflows for day-to-day development loops.

## Files and locations
- `guides/dev/python.md` - Python runtime and environment command patterns.
- `guides/dev/flutter.md` - Flutter app lifecycle commands.
- `guides/dev/flutter-pub.md` - dependency and package workflows for Flutter/Dart.
- `guides/dev/cargo.md` - Rust build/test/release commands.

## Recommended order
1. `python.md`
2. `flutter.md`
3. `flutter-pub.md`
4. `cargo.md`

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `python -m venv .venv` | Create isolated Python environment |
| `source .venv/bin/activate` | Activate Python virtual environment |
| `python -m pip install -U pip` | Upgrade pip in active environment |
| `uv sync` | Install dependencies from lockfile with uv |
| `uv run pytest -q` | Run tests in uv-managed environment |
| `flutter pub get` | Resolve Flutter dependencies |
| `flutter run -d linux` | Run Flutter app on Linux target |
| `flutter test` | Run Flutter test suite |
| `dart pub outdated` | Check dependency upgrade opportunities |
| `cargo check` | Fast compile-time validation |
| `cargo test` | Execute Rust test suite |
| `cargo clippy --all-targets --all-features` | Run strict linting for Rust code |
