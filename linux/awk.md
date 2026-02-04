# awk — text processing by columns
# Use it to slice, filter, and aggregate text.

- `awk '{print $1}' file` — print first column
- `awk -F, '{print $1}' file` — comma‑separated fields
- `awk 'NR==1{print}' file` — first line only
- `awk '$3 > 10' file` — filter by column value
- `awk '{sum+=$3} END{print sum}' file` — sum column
