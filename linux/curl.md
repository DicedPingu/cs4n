# curl - HTTP client for APIs and transfers
# Use it for API calls, diagnostics, uploads, and scripted downloads.

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

