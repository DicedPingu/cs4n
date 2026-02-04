# chmod Quicksheet

Change file permissions.

## basics

- `chmod 644 file.txt`
  - What it does: Sets permissions to rw-r--r--.
  - When to use it: Standard readable files.
- `chmod 755 script.sh`
  - What it does: Sets permissions to rwxr-xr-x.
  - When to use it: Executable scripts.
- `chmod +x script.sh`
  - What it does: Adds execute permission.
  - When to use it: Making a script runnable.

## symbolic modes

- `chmod u+w file.txt`
  - What it does: Adds write permission for owner.
  - When to use it: Fixing a read-only file.
- `chmod g-r file.txt`
  - What it does: Removes read permission for group.
  - When to use it: Restricting group access.
- `chmod o= file.txt`
  - What it does: Removes all permissions for others.
  - When to use it: Private files.

## recursive

- `chmod -R 755 dir/`
  - What it does: Recursively sets permissions.
  - When to use it: Fixing a whole directory tree.
- `chmod -R u+X dir/`
  - What it does: Adds execute on dirs and already-executable files.
  - When to use it: Safe recursive execute.

# chown Quicksheet

Change file ownership.

## basics

- `chown user file.txt`
  - What it does: Changes the file owner.
  - When to use it: Fixing ownership after sudo actions.
- `chown user:group file.txt`
  - What it does: Changes owner and group.
  - When to use it: Matching project ownership.
- `chown :group file.txt`
  - What it does: Changes group only.
  - When to use it: Group access adjustments.

## recursive

- `chown -R user:group dir/`
  - What it does: Recursively changes owner and group.
  - When to use it: Repairing a folder tree.

## references

- `chown --reference=src.txt target.txt`
  - What it does: Copies owner/group from another file.
  - When to use it: Matching permissions quickly.
