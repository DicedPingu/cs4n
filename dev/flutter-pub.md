# Flutter Pub — Flutter dependency manager
# Use it to add, update, and inspect Flutter deps.

## Add / remove
- `flutter pub add <pkg>` — add dep
- `flutter pub add dev:<pkg>` — add dev dep
- `flutter pub remove <pkg>` — remove dep

## Install / update
- `flutter pub get` — install deps
- `flutter pub upgrade` — update within constraints
- `flutter pub upgrade --major-versions` — allow breaking upgrades
- `flutter pub downgrade` — lowest versions

## Inspect
- `flutter pub outdated` — list newer versions
- `flutter pub deps` — dependency tree

## Cache
- `flutter pub cache repair` — fix cache
