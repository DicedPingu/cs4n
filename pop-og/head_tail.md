# head & tail

`head` and `tail` are utilities for viewing the beginning or end of files. They are essential for inspecting logs or large data files without opening the entire file.

## head

By default, `head` prints the first 10 lines of each file.

```bash
head filename.txt
```

### Specify Number of Lines

Use `-n` to specify a different number of lines:

```bash
head -n 5 filename.txt
```

## tail

By default, `tail` prints the last 10 lines of each file.

```bash
tail filename.txt
```

### Follow Mode (Live Updates)

The most powerful feature of `tail` is the `-f` (follow) flag, which allows you to watch a file as it grows. This is incredibly useful for monitoring logs.

```bash
tail -f /var/log/syslog
```

### Specify Number of Lines

Like head, you can view a specific number of lines from the end:

```bash
tail -n 20 filename.txt
```

## Combined Usage

You can combine them to view a specific section of a file (e.g., lines 10-20):

```bash
head -n 20 filename.txt | tail -n 10
```
