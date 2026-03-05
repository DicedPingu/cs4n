# fwupd - Linux firmware update tooling
Use it to discover devices, refresh metadata, and apply firmware updates.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Recommended update flow
- `fwupdmgr get-devices` - list updatable hardware.
- `fwupdmgr refresh --force` - refresh LVFS metadata.
- `fwupdmgr get-updates` - check available firmware.
- `sudo fwupdmgr update` - apply updates.

## Useful diagnostics
- `fwupdmgr security` - security status overview.
- `fwupdmgr get-history` - recent update history.
- `fwupdmgr get-remotes` - active metadata remotes.

## Operational notes
- Keep AC power connected for laptop firmware updates.
- Reboots are often required; schedule updates outside active work windows.

## Version and release line
- Local check: `fwupdmgr --version`
- Upstream release snapshot: fwupd `2.0.19`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `fwupdmgr get-devices` | Display all devices detected by `fwupd` |
| `fwupdmgr refresh` | Download the latest firmware metadata from LVFS |
| `fwupdmgr get-updates` | List the updates available for devices on your system |
| `fwupdmgr update` | Install firmware updates |
| `sudo mount [-o\|--options] uid=1000,gid=1000,umask=0022 /dev/sdX /boot` | Remount `/boot` with more privileges if update complains about a read-only filesystem |
| `fwupdmgr get-history` | Show firmware update history |
| `fwupdmgr --help` | Show command usage and option reference |
| `man fwupdmgr` | Open the full manual page |
| `whatis fwupdmgr` | Print one-line command description |
| `type -a fwupdmgr` | Show how the shell resolves the command path |
| `command -v fwupdmgr` | Print executable path used by current shell |
| `tldr fwupdmgr` | Show concise command examples |
| `apropos fwupdmgr` | Search manual database for related commands |
| `fwupdmgr --version` | Print local tool version |
