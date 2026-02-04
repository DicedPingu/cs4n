# tar — archive files
# Use it to create and extract tarballs.

- `tar -czf out.tgz dir/` — create .tgz
- `tar -xzf out.tgz` — extract .tgz
- `tar -tf out.tgz` — list contents
- `tar -C /dest -xzf out.tgz` — extract to dir
- `tar --exclude '*.log' -czf out.tgz dir/` — exclude files
