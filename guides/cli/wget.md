# wget - non-interactive downloader
Use it for resilient scripted downloads and recursive site fetches.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

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

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `wget https://example.com/foo` | Download the contents of a URL to a file (named "foo" in this case) |
| `wget [-O\|--output-document] bar https://example.com/foo` | Download the contents of a URL to a file (named "bar" in this case) |
| `wget [-pkw\|--page-requisites --convert-links --wait] 3 https://example.com/some_page.html` | Download a single web page and all its resources with 3-second intervals between requests (scripts, stylesheets, images, etc.) |
| `wget [-mnp\|--mirror --no-parent] https://example.com/some_path/` | Download all listed files within a directory and its sub-directories (does not download embedded page elements) |
| `wget --limit-rate 300k [-t\|--tries] 100 https://example.com/some_path/` | Limit the download speed and the number of connection retries |
| `wget --user username --password password https://example.com` | Download a file from an HTTP server using Basic Auth (also works for FTP) |
| `wget [-c\|--continue] https://example.com` | Continue an incomplete download |
| `wget [-P\|--directory-prefix] path/to/directory [-i\|--input-file] path/to/URLs.txt` | Download all URLs stored in a text file to a specific directory |
| `wget --help` | Show command usage and option reference |
| `man wget` | Open the full manual page |
| `whatis wget` | Print one-line command description |
| `type -a wget` | Show how the shell resolves the command path |
| `command -v wget` | Print executable path used by current shell |
| `tldr wget` | Show concise command examples |
| `apropos wget` | Search manual database for related commands |
| `wget --version` | Print local tool version |
