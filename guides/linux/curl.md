# curl - HTTP client for APIs and transfers
Use it for API calls, diagnostics, uploads, and scripted downloads.

## Read This Command Syntax
- `<value>` means replace with your real value.
- `[value]` means optional input.
- `-x` is a short flag; `--long` is the long form of an option.
- Run the safest/dry-run example first when available, then the destructive version.

## Core request patterns
- `curl -L https://example.com` - GET and follow redirects.
- `curl -I https://example.com` - headers only.
- `curl -o out.bin https://example.com/file` - write to custom filename.
- `curl -O https://example.com/file` - keep remote filename.

## API workflows
- `curl -sS --fail https://api.example.com/items` - clean failure handling.
- `curl -X POST -H "Content-Type: application/json" -d '{"k":"v"}' https://api.example.com/items` - JSON POST.
- `curl -H "Authorization: Bearer $TOKEN" https://api.example.com/me` - bearer auth.

## Reliability flags
- `curl --retry 5 --retry-delay 2 --retry-all-errors <url>` - robust retries.
- `curl --connect-timeout 5 --max-time 30 <url>` - timeout boundaries.
- `curl --fail-with-body <url>` - non-zero exit on HTTP errors while retaining body.

## Debugging and traces
- `curl -v <url>` - request/response details.
- `curl --trace-ascii trace.log <url>` - detailed transport trace.

## Version and release line
- Local check: `curl --version`
- Upstream release snapshot: curl `8.18.0`.

## Expanded Cheats (2026-03)
More command/subcommand/option examples you can run directly.

| Command | Use case |
| --- | --- |
| `curl https://example.com` | Make an HTTP GET request and dump the contents in `stdout` |
| `curl [-L\|--location] [-D\|--dump-header] - https://example.com` | Make an HTTP GET request, follow any `3xx` redirects, and dump the reply headers and contents to `stdout` |
| `curl [-O\|--remote-name] https://example.com/filename.zip` | Download a file, saving the output under the filename indicated by the URL |
| `curl [-X\|--request] POST [-d\|--data] 'name=bob' http://example.com/form` | Send form-encoded data (POST request of type `application/x-www-form-urlencoded`). Use `--data @file_name` or `--data @'-'` to read from `stdin` |
| `curl [-k\|--insecure] [-x\|--proxy] http://127.0.0.1:8080 [-H\|--header] 'Authorization: Bearer token' [-X\|--request] GET\|PUT\|POST\|DELETE\|PATCH\|... https://example.com` | Send a request with an extra header, using a custom HTTP method and over a proxy (such as BurpSuite), ignoring insecure self-signed certificates |
| `curl [-d\|--data] '{"name":"bob"}' [-H\|--header] 'Content-Type: application/json' http://example.com/users/1234` | Send data in JSON format, specifying the appropriate Content-Type header |
| `curl [-E\|--cert] client.pem --key key.pem [-k\|--insecure] https://example.com` | Pass client certificate and private key for the request, skipping certificate validation |
| `curl [-v\|--verbose] --resolve example.com:80:127.0.0.1 http://example.com` | Resolve a hostname to a custom IP address, with verbose output (similar to editing the `/etc/hosts` file for custom DNS resolution) |
| `curl --help` | Show command usage and option reference |
| `man curl` | Open the full manual page |
| `whatis curl` | Print one-line command description |
| `type -a curl` | Show how the shell resolves the command path |
| `command -v curl` | Print executable path used by current shell |
| `tldr curl` | Show concise command examples |
| `apropos curl` | Search manual database for related commands |
| `curl --version` | Print local tool version |
