# SH-051 — Find Empty Files

**Description**

List regular files of size zero beneath a provided directory.

**Tips**

`find` can filter files by size with `-empty` or a size predicate, but the task is about regular files only. Restrict the search root and type so empty directories are not included. Be careful with names containing spaces or newlines and avoid deleting anything as part of the search.

**What you need to know:** Learn `find -type f -empty` and distinguish empty files from empty directories.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./data/empty.txt
```
