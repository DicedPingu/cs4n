# Flutter - cross-platform UI SDK
Use it to build mobile, web, and desktop applications from one Dart codebase.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Environment readiness
- `flutter --version` - SDK and channel info.
- `flutter doctor -v` - full environment diagnostics.
- `flutter config --list` - platform/tooling settings.

## New app workflow
- `flutter create my_app` - scaffold app.
- `cd my_app`
- `flutter pub get` - dependency resolution.
- `flutter run -d <device-id>` - launch app.

## Build targets
- `flutter build apk --release` - Android APK.
- `flutter build appbundle --release` - Play Store bundle.
- `flutter build ios --release` - iOS artifact generation.
- `flutter build web --release` - optimized web bundle.
- `flutter build linux|windows|macos --release` - desktop binaries.

## Debug and performance flow
- `flutter run --profile` - profile mode for perf work.
- `flutter logs` - device/app logs.
- `flutter attach` - attach to running app process.
- `flutter symbolize -i stack.txt -d symbols/` - decode crash symbols.

## Quality gates
- `flutter analyze` - static analysis.
- `flutter test` - unit/widget tests.
- `flutter test integration_test` - integration tests.

## Version and release line
- Local check: `flutter --version`
- Stable release snapshot: Flutter `3.38.9` (2026-02-08 snapshot).

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
