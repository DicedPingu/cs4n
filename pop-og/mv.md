# mv Quicksheet
Move or rename files.

## basics
- `mv old.txt new.txt`
  - What it does: Renames a file.
  - When to use it: Simple renames.
- `mv file.txt dir/`
  - What it does: Moves a file into a directory.
  - When to use it: Reorganizing files.
- `mv dir/ new-dir/`
  - What it does: Renames a directory.
  - When to use it: Folder re-labeling.

## safety and feedback
- `mv -i file.txt dir/`
  - What it does: Prompts before overwrite.
  - When to use it: Avoiding accidental clobber.
- `mv -n file.txt dir/`
  - What it does: Never overwrites existing files.
  - When to use it: Conservative moves.
- `mv -v file.txt dir/`
  - What it does: Verbose output.
  - When to use it: Seeing what moved.

## patterns
- `mv *.log archive/`
  - What it does: Moves all .log files to a folder.
  - When to use it: Quick cleanup.
- `mv --backup=numbered file.txt dir/`
  - What it does: Keeps numbered backups if a file exists.
  - When to use it: Safer batch moves.
