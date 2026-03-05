# Dart Pub - Dart package manager
Use it in pure Dart projects (or from Flutter tooling when you need raw Dart commands).

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `dart create project_name` | Initialize a new Dart project in a directory of the same name |
| `dart run path/to/file.dart` | Run a Dart file |
| `dart pub get` | Download dependencies for the current project |
| `dart test` | Run unit tests for the current project |
| `dart pub upgrade --null-safety` | Update an outdated project's dependencies to support null-safety |
| `dart compile exe path/to/file.dart` | Compile a Dart file to a native binary |
| `dart fix --apply` | Apply automated fixes to the current project |
| `dart --help` | Show command usage and option reference |
| `man dart` | Open the full manual page |
| `whatis dart` | Print one-line command description |
| `type -a dart` | Show how the shell resolves the command path |
| `command -v dart` | Print executable path used by current shell |
| `tldr dart` | Show concise command examples |
| `apropos dart` | Search manual database for related commands |
| `dart --version` | Print local tool version |
| `flutter create project_name` | Initialize a new Flutter project in a directory of the same name |
| `flutter doctor` | Check if all external tools are correctly installed |
| `flutter channel stable\|beta\|dev\|master` | List or change Flutter channel |
| `flutter run -d all` | Run Flutter on all started emulators and connected devices |
| `flutter test test/example_test.dart` | Run tests in a terminal from the root of the project |
