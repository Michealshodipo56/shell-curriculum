# SH-075 — Test a Shell Script

**Description**

Write a shell-based test harness that runs a supplied utility with valid and invalid inputs and checks output and exit status.

**Tips**

Shell scripts can be tested by invoking them with controlled fixtures and comparing stdout, stderr, exit status, and filesystem effects. Create temporary test directories and clean them afterward. Include success cases, invalid input, spaces in paths, and repeat runs. Do not rely solely on visual inspection of sample output.

**What you need to know:** Learn temporary fixtures, output capture, expected statuses, and why tests should isolate their working directory.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
PASS valid input
PASS missing file
2 tests passed
```
