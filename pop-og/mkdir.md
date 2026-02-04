# mkdir Quicksheet
Create directories.

## basics
- `mkdir new-folder`
  - What it does: Creates a single directory.
  - When to use it: Simple folder creation.
- `mkdir -p path/to/new-folder`
  - What it does: Creates parent directories as needed.
  - When to use it: Deep paths in one command.
- `mkdir -m 755 public/`
  - What it does: Creates a directory with a specific mode.
  - When to use it: Setting permissions at creation.

## patterns
- `mkdir -p logs/{app,db,nginx}`
  - What it does: Creates multiple directories with brace expansion.
  - When to use it: Quick project scaffolding.
- `mkdir -p {src,tests,docs}`
  - What it does: Creates standard project folders.
  - When to use it: New repo setup.
