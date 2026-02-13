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

