# curl Quicksheet
Transfer data from URLs.

## basics
- `curl https://example.com`
  - What it does: Fetches a URL and prints to stdout.
  - When to use it: Quick checks and simple downloads.
- `curl -o file.zip https://example.com/file.zip`
  - What it does: Saves output to a file.
  - When to use it: Downloading files with a custom name.
- `curl -L https://example.com`
  - What it does: Follows redirects.
  - When to use it: Short links and CDN redirects.

## APIs
- `curl -X GET https://api.example.com/items`
  - What it does: Sends a GET request.
  - When to use it: API reads.
- `curl -X POST -H 'Content-Type: application/json' -d '{"name":"test"}' https://api.example.com/items`
  - What it does: Sends JSON data.
  - When to use it: Creating resources.
- `curl -H 'Authorization: Bearer TOKEN' https://api.example.com/me`
  - What it does: Adds an auth header.
  - When to use it: Secured endpoints.

## debugging
- `curl -I https://example.com`
  - What it does: Fetches headers only.
  - When to use it: Checking status and response headers.
- `curl -v https://example.com`
  - What it does: Verbose output.
  - When to use it: Debugging TLS or redirects.
