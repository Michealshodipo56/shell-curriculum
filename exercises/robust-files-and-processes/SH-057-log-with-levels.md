# SH-057 — Log With Levels

**Description**

Write reusable logging functions for INFO, WARN, and ERROR with timestamps, sending errors to stderr.

**Tips**

Structured logs help distinguish informational messages, warnings, and errors. Use a small logging function that accepts a level and message, prepends a timestamp, and writes to the intended stream or file. Keep formatting consistent and never put credentials into logs. Confirm that error messages are visible on stderr.

**What you need to know:** Learn `printf`, date formatting, output streams, and why structured, consistent logs help debugging.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
2026-11-17T09:00:00 INFO started
```
