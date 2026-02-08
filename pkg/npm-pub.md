# Dart Pub - Dart package manager
# Use it in pure Dart projects (or from Flutter tooling when you need raw Dart commands).

## Typical project loop
- `dart pub get` - resolve/install dependencies.
- `dart pub add <pkg>` - add runtime dependency.
- `dart pub add dev:<pkg>` - add dev dependency.
- `dart pub remove <pkg>` - remove dependency.
- `dart pub deps` - inspect resolved graph.

## Upgrades with control
- `dart pub outdated` - compare constraints vs latest releases.
- `dart pub upgrade` - upgrade within current constraints.
- `dart pub upgrade --major-versions` - rewrite constraints to newer majors.
- `dart pub downgrade` - test lowest compatible versions.

## Package publishing checklist
- `dart analyze` - static analysis must be clean.
- `dart test` - verify behavior before publish.
- `dart pub publish --dry-run` - validate package metadata and contents.
- `dart pub publish` - publish to pub.dev.

## Useful options
- `--directory <path>` - run pub commands for a different project root.
- `--offline` - avoid network resolution when cache is present.

## Version and release line
- Local check: `dart --version`
- Stable line snapshot: Dart `3.10.9` (released 2026-02-03).
- Track official archive: `dart-archive/channels/stable/release/latest/VERSION`.

