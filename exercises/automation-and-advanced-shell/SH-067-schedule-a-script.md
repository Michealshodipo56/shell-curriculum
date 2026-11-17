# SH-067 — Schedule a Script

**Description**

Write a script suitable for scheduled execution and document a cron entry that runs it daily at 02:00.

**Requirements**

Learn cron’s five time fields, minimal environment, absolute paths, output redirection, and timezone considerations.

**Tips**

`cron` runs commands on a schedule using five time fields followed by a command. Cron has a minimal environment and often a different working directory, so scripts should use absolute paths and explicit logging. For this exercise, prepare or explain the schedule without modifying system-wide jobs unless the environment specifically allows it.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
0 2 * * * /absolute/path/job.sh
```
