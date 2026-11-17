# SH-055 — Stop Gracefully

**Description**

Write a long-running script that handles SIGINT and SIGTERM by cleaning up and exiting.

**Requirements**

Learn `trap`, signals, interruption, and idempotent cleanup. Do not assume SIGKILL can be trapped.

**Tips**

Signals tell processes about events such as interruption or termination. `trap` registers a handler for signals or shell exit; use it to clean temporary resources and exit predictably. Avoid traps that swallow errors or recursively trigger themselves. Test with a harmless long-running script rather than a system service.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
received termination signal; cleaned up
```
