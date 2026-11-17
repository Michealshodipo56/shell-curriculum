# SH-030 — Quote It Correctly

**Description**

Write a script that creates a file using a filename supplied as an argument, including filenames containing spaces.

**Requirements**

Learn double quoting, word splitting, glob expansion, and safe argument handling; never build command strings using `eval`.

**Tips**

Unquoted expansions can undergo word splitting and pathname globbing, which changes the number of arguments a command receives. Double quotes preserve the expanded value as one argument; single quotes keep characters literal. Compare behavior with spaces and `*` characters in test values. Quote path and user-input expansions unless you deliberately want splitting.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./make-file.sh "my notes.txt" → my notes.txt created
```
