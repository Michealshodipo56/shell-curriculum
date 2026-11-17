# SH-052 — Safe Temporary Workspace

**Description**

Create a temporary directory, write an intermediate file, and remove the temporary directory on normal exit or interruption.

**Requirements**

Learn `mktemp -d`, `trap`, safe quoting, and cleanup for EXIT; consider signal behavior.

**Tips**

`mktemp -d` creates a unique temporary directory and helps avoid collisions. Store the generated path and register a cleanup `trap` so temporary files are removed when the script exits. Quote the path in every operation and ensure cleanup cannot target an empty or unintended location.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
temporary work completed; no temporary directory remains
```
