# SH-026 — Accept Positional Arguments

**Description**

Write a script that accepts a first name and surname as two command-line arguments and prints them together.

**Requirements**

Learn `$1`, `$2`, `$#`, and argument validation. Always quote positional expansions.

**Tips**

Command-line arguments become positional parameters: `$1` is the first, `$2` the second, and `$#` counts how many were supplied. Quote each expansion to preserve names with spaces. Validate the argument count before formatting the output so a missing surname does not silently produce a misleading result.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./full-name.sh Ada Lovelace → Ada Lovelace
```
