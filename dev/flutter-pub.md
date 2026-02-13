# Flutter Pub - Flutter dependency workflow
Use it to manage package dependencies in Flutter app/plugin projects.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Daily dependency operations
- `flutter pub get` - resolve and install dependencies.
- `flutter pub add <pkg>` - add runtime package.
- `flutter pub add dev:<pkg>` - add development package.
- `flutter pub remove <pkg>` - remove dependency.

## Upgrade strategy
- `flutter pub outdated` - compare constraints to latest releases.
- `flutter pub upgrade` - upgrade within declared ranges.
- `flutter pub upgrade --major-versions` - rewrite constraints to newer majors.
- `flutter pub downgrade` - validate minimum supported versions.

## Build hygiene around dependency updates
- `flutter clean && flutter pub get` - reset artifact drift.
- `flutter analyze` - static checks after upgrades.
- `flutter test` - regression check.

## Cache and network recovery
- `flutter pub cache repair` - rebuild pub cache.
- `flutter pub cache clean` - clear stale cache entries.

## Version and release line
- Local check: `flutter --version && dart --version`
- Stable snapshot lines: Flutter `3.38.9`, Dart `3.10.9`.

