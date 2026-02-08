# Flutter - cross-platform UI SDK
# Use it to build mobile, web, and desktop applications from one Dart codebase.

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

