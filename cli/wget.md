# wget — download files and websites
# Use it for scripted downloads and mirrors.

## Basic
- `wget <url>` — download to current folder
- `wget -O <file> <url>` — save as specific filename
- `wget -P <dir> <url>` — download into a directory
- `wget -c <url>` — resume partial download

## Mirrors / sites
- `wget -r <url>` — recursive download
- `wget -r -np <url>` — no parent directories
- `wget --mirror <url>` — mirror (recursive + timestamp)
- `wget --convert-links -r <url>` — fix links for local viewing

## Auth / headers
- `wget --user <u> --password <p> <url>` — basic auth
- `wget --header="Authorization: Bearer ..." <url>` — custom header
- `wget --user-agent="UA" <url>` — custom UA

## Control
- `wget -q <url>` — quiet
- `wget --show-progress <url>` — progress bar
- `wget --limit-rate=1m <url>` — throttle
- `wget --timeout=10 --tries=3 <url>` — retry behavior
