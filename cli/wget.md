# wget - non-interactive downloader
# Use it for resilient scripted downloads and recursive site fetches.

## Core download patterns
- `wget <url>` - download to current directory.
- `wget -O artifact.tar.gz <url>` - custom output filename.
- `wget -P downloads/ <url>` - write into target directory.
- `wget -c <url>` - continue partial download.

## Reliability and throttling
- `wget --tries=5 --timeout=15 <url>` - retry envelope.
- `wget --waitretry=2 --retry-connrefused <url>` - better transient failure handling.
- `wget --limit-rate=1m <url>` - bandwidth cap.
- `wget --show-progress <url>` - readable progress.

## Auth and request customization
- `wget --header="Authorization: Bearer $TOKEN" <url>` - token auth.
- `wget --user <user> --password <pass> <url>` - basic auth.
- `wget --user-agent="my-agent/1.0" <url>` - custom user agent.

## Recursive/site fetch use-cases
- `wget -r -np <url>` - recursive download without parent traversal.
- `wget --mirror --convert-links --adjust-extension <url>` - local static mirror.

## Version and release line
- Local check: `wget --version`
- Upstream release snapshot: GNU Wget `1.25.0`.

