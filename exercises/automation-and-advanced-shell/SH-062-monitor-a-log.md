# SH-062 — Monitor a Log

**Description**

Follow newly appended lines in a log and print only those matching a supplied keyword until interrupted.

**Tips**

`tail -f` follows a growing file, but a production monitor must consider interruption and log rotation. Decide how to recognize new matching lines and where to send alerts. Keep the exercise's scope limited to the supplied log and provide a clean way to stop. Test by appending a line after the monitor starts.

**What you need to know:** Learn `tail -f` or `tail -F`, pipes, buffering, and graceful termination.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
new line: ERROR database unavailable
```
