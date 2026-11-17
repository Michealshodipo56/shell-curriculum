# SH-056 — Prevent Concurrent Runs

**Description**

Ensure two instances of a script cannot modify the same output at once.

**Requirements**

Learn advisory locking with `flock` on Linux or an atomic-directory strategy; explain cleanup and stale-lock concerns.

**Tips**

A lock prevents two copies of a script from changing the same resources simultaneously. `flock` can lock a file descriptor on Linux; an atomic directory-creation strategy is another option with cleanup considerations. Acquire the lock before doing work and release it on exit. A second invocation should fail or wait according to the task's specification.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
second run → already running (exit 1)
```
