# SH-012 — Append an Activity Log

**Description**

Add a new timestamped message to `activity.log` without deleting existing entries.

**Requirements**

Study `>>`, the `date` command, and the difference between overwrite and append. The timestamp format should be documented.

**Tips**

`>>` appends to a file instead of truncating it. `date` can format a timestamp using a pattern such as `+%Y-%m-%d\ %H:%M:%S`; the backslash here illustrates escaping a space in a format argument. Build one complete log record and append it as a single line. Confirm old records remain unchanged and new entries appear at the end.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
2026-11-17 09:00:00 started
```
