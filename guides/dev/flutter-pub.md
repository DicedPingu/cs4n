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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `flutter create project_name` | Initialize a new Flutter project in a directory of the same name |
| `flutter doctor` | Check if all external tools are correctly installed |
| `flutter channel stable\|beta\|dev\|master` | List or change Flutter channel |
| `flutter run -d all` | Run Flutter on all started emulators and connected devices |
| `flutter test test/example_test.dart` | Run tests in a terminal from the root of the project |
| `flutter build apk --target-platform android-arm,android-arm64` | Build a release APK targeting most modern smartphones |
| `flutter clean` | Delete the `build` and `.dart_tool` directories |
| `flutter help command` | Display help about a specific command |
| `flutter --help` | Show command usage and option reference |
| `man flutter` | Open the full manual page |
| `whatis flutter` | Print one-line command description |
| `type -a flutter` | Show how the shell resolves the command path |
| `command -v flutter` | Print executable path used by current shell |
| `tldr flutter` | Show concise command examples |
| `apropos flutter` | Search manual database for related commands |
| `flutter --version` | Print local tool version |
| `dart create project_name` | Initialize a new Dart project in a directory of the same name |
| `dart run path/to/file.dart` | Run a Dart file |
| `dart pub get` | Download dependencies for the current project |
| `dart test` | Run unit tests for the current project |
