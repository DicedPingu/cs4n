# Flutter (Practical Workflow Cheatsheet)

## 1) Setup / health
- `flutter --version`
- `flutter doctor -v`
- `flutter upgrade`

## 2) New project (ordered)
1) `flutter create <app_name>`
2) `cd <app_name>`
3) `flutter pub get`
4) `flutter run`

## 3) Run & debug
- `flutter run`
- `flutter run -d <device_id>`
- `flutter run --release` (perf testing)
- `flutter run --profile`
- `flutter attach`
- `flutter logs`

## 4) Build
- `flutter build apk`
- `flutter build appbundle`
- `flutter build ios`
- `flutter build web`
- `flutter build linux | macos | windows`

## 5) Test / analyze
- `flutter analyze`
- `flutter test`

## 6) Devices / emulators
- `flutter devices`
- `flutter emulators`
- `flutter emulators --launch <emulator_id>`

## 7) Dependencies
- `flutter pub get`
- `flutter pub add <package>`
- `flutter pub upgrade`
- `flutter pub outdated`

## 8) Cleanup / cache
- `flutter clean`
- `flutter precache`
