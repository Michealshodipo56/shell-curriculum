# SH-053 — Check a Dependency

**Description**

Verify that a required external command is installed before running a task; otherwise print a useful error and exit nonzero.

**Tips**

`command -v` checks whether an executable can be resolved on `PATH` without running it. When a required dependency is missing, print a helpful message to stderr and exit nonzero before starting work. Avoid hardcoding `/usr/bin` locations, since different systems install tools in different directories.

**What you need to know:** Learn `command -v`, stderr messages, and why explicit dependency checks improve portability.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
error: required command jq is missing
```
