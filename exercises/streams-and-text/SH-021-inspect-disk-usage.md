# SH-021 — Inspect Disk Usage

**Description**

Report the human-readable total size of a supplied directory and the free space on its filesystem.

**Requirements**

Learn `du -sh` and `df -h`; explain used directory space versus available filesystem capacity.

**Tips**

`du` estimates space occupied by a directory tree, while `df` reports filesystem capacity and free space. `-s` summarizes a directory instead of listing every child, and `-h` formats byte counts for humans. They answer different questions and may report different units. Label both values clearly rather than confusing directory size with free disk space.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
directory: 24K; filesystem available: 8.2G
```
