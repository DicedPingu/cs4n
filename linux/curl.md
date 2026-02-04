# curl — HTTP client for APIs and downloads
# Use it for requests, uploads, and debugging.

- `curl <url>` — GET request
- `curl -L <url>` — follow redirects
- `curl -O <url>` — save with remote name
- `curl -o file <url>` — save with custom name
- `curl -I <url>` — headers only
- `curl -sS <url>` — silent but show errors
- `curl --fail <url>` — non‑zero on 4xx/5xx
- `curl -X POST -H "Content-Type: application/json" -d '{...}' <url>` — POST JSON
- `curl --retry 3 --retry-delay 2 <url>` — retry on failure
