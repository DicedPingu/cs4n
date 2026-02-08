# head / tail - view beginning or end of files
# Use them for quick sampling and live log monitoring.

## Daily use
- `head -n 30 file` - first lines.
- `tail -n 30 file` - last lines.
- `tail -f app.log` - follow appended lines.
- `tail -F app.log` - follow across log rotation.

## Precision patterns
- `head -c 200 file.bin` - first N bytes.
- `tail -c 200 file.bin` - last N bytes.
- `tail -n +50 file` - start from line 50.

## Good combinations
- `tail -f app.log | grep -i error` - live error filter.
- `head -n 1 file && tail -n 1 file` - check boundaries quickly.

## Version and release line
- Local check: `head --version && tail --version`
- Upstream release snapshot: GNU coreutils `9.10`.

