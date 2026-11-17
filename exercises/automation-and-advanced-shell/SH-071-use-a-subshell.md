# SH-071 — Use a Subshell

**Description**

Run a command in a supplied directory without changing the caller’s working directory.

**Requirements**

Learn `( ... )` subshell grouping and how directory changes and variable assignments are isolated.

**Tips**

Parentheses run commands in a subshell, isolating changes such as `cd` and variable assignments from the caller. Braces group commands in the current shell instead. Compare the working directory and variables before and after the grouped commands. Use the isolation deliberately rather than relying on accidental scope behavior.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
before=/home/ada
inside=/tmp
after=/home/ada
```
