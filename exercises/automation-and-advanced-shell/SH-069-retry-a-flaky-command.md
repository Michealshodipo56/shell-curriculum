# SH-069 — Retry a Flaky Command

**Description**

Run a supplied command up to a configurable maximum number of attempts, waiting between failures and stopping immediately on success.

**Tips**

Retries are useful for transient failures, but not for permanent validation errors. Attempt the command a bounded number of times, inspect each exit status, and delay between attempts with `sleep`. Consider increasing delays and stop immediately on success. Report failure only after the final permitted attempt.

**What you need to know:** Learn retries, exit statuses, bounded loops, delays, and why some operations are unsafe to retry.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
attempt 1 failed
attempt 2 succeeded
```
