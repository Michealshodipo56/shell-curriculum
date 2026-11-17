# SH-061 — Backup With Rotation

**Description**

Back up a specified directory to timestamped archives and retain only the newest N backups.

**Tips**

Backup rotation keeps a bounded number of prior archives. Create a new uniquely named backup, verify it, then identify old backups using a stable naming convention before pruning. Sort by a reliable timestamp or sequence and avoid deleting unrelated files. Think about partial failures and never remove the only good backup first.

**What you need to know:** Learn timestamp naming, sorting, retention rules, and safe deletion restricted to a dedicated backup directory.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
backup-20261117-090000.tar.gz created; 3 retained
```
