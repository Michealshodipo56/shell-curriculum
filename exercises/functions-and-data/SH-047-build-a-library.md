# SH-047 — Build a Library

**Description**

Move reusable validation and formatting functions into `lib.sh` and load them from a second script.

**Requirements**

Learn `source`/`.` and how sourcing executes code in the current shell; resolve library paths relative to the script.

**Tips**

A shared library can hold reusable functions that other scripts load with `source` or `.`. Sourcing executes the file in the current shell, so it should define functions without unexpectedly running the program's main behavior. Use a predictable relative or absolute library path and test calling its functions from a separate script.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./main.sh 12 → valid: 12
```
