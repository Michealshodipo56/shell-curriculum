# SH-043 — Return Status, Print Data

**Description**

Define a function that checks whether a supplied path is readable and use its exit status to print a result.

**Tips**

A function's `return` sets an integer status code, not an arbitrary string result. Print data on stdout and capture it with command substitution `$(...)` when appropriate; reserve stderr for errors. Keep success status zero and use nonzero codes for failures. Avoid mixing debug messages into data output.

**What you need to know:** Learn that `return` communicates an integer status (0–255), while stdout carries text results.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
notes.txt → readable
```
