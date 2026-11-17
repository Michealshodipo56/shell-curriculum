# SH-050 — Read Every Line

**Description**

Print numbered lines from a supplied text file, preserving leading spaces and backslashes.

**Tips**

`IFS= read -r line` is the standard pattern for preserving leading whitespace and backslashes when reading a file line by line. A final line without a newline needs special attention. Redirect the file into the loop instead of piping into it if variables updated in the loop must remain available afterward.

**What you need to know:** Use `while IFS= read -r line || [[ -n $line ]]` to handle the final line without a newline.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
1: alpha
2: beta
```
