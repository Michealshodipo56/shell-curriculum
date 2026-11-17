# SH-059 — Archive a Directory

**Description**

Create a compressed `.tar.gz` archive of a supplied directory with a predictable output filename.

**Tips**

`tar` collects a directory tree into an archive, and compression may be enabled with `-z` for gzip. Decide whether the archive should include the parent directory or only its contents. Use predictable source and destination paths, avoid archiving the output into itself, and verify the command succeeds.

**What you need to know:** Learn `tar -czf`, relative archive paths, quoting, and how to inspect an archive before trusting it.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
project/ → project.tar.gz
```
