# SH-054 — Understand Process IDs

**Description**

Start a short-lived background command, print its PID, wait for it, and report its exit status.

**Requirements**

Learn `&`, `$!`, `wait`, and the difference between parent and child processes.

**Tips**

`$` identifies the current shell process, while `$!` refers to the PID of the most recently started background job. Start a controlled background process, record its PID, and use `wait` to collect its completion status. Do not assume a PID stays valid forever or belongs to the same process after it exits.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
started PID 1234
finished status 0
```
