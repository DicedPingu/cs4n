# Flutter — UI toolkit for mobile, desktop, and web
# Use it to build and ship cross‑platform apps.

## 1) Setup / health
- `flutter --version` — SDK version
- `flutter doctor -v` — environment check
- `flutter upgrade` — update SDK

## 2) New project (ordered)
- `flutter create <app>` — create app
- `flutter create --platforms=android,web <app>` — limit platforms
- `cd <app>`
- `flutter pub get` — fetch deps
- `flutter run` — run app

## 3) Run & debug
- `flutter run -d <id>` — run on device
- `flutter run --profile` — perf profiling
- `flutter run --release` — release build on device
- `flutter run --dart-define=KEY=VALUE` — build‑time config
- `flutter attach` — attach to running app
- `flutter logs` — device logs

## 4) Build
- `flutter build apk` — Android APK
- `flutter build apk --split-per-abi` — smaller APKs
- `flutter build appbundle` — Android AAB
- `flutter build ios` — iOS build
- `flutter build web` — web build
- `flutter build linux|macos|windows` — desktop builds

## 5) Test / analyze
- `flutter analyze` — static analysis
- `flutter test` — tests

## 6) Devices / emulators
- `flutter devices` — connected devices
- `flutter emulators` — available emulators
- `flutter emulators --launch <id>` — start emulator

## 7) Cleanup / cache
- `flutter clean` — remove build outputs
- `flutter precache` — download artifacts
