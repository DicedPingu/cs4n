# Dart Pub — Dart package manager
# Use it when you’re in pure Dart projects (not Flutter).

## Add / remove
- `dart pub add <pkg>` — add dep
- `dart pub add dev:<pkg>` — add dev dep
- `dart pub remove <pkg>` — remove dep

## Install / update
- `dart pub get` — install deps
- `dart pub upgrade` — update within constraints
- `dart pub upgrade --major-versions` — allow breaking upgrades
- `dart pub downgrade` — lowest versions

## Inspect
- `dart pub outdated` — list newer versions
- `dart pub deps` — dependency tree
