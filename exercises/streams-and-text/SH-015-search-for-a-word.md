# SH-015 — Search for a Word

**Description**

Print every line in a provided file containing the word `error`, ignoring letter case.

**Requirements**

Learn `grep -i`, matching substrings, and why quotes help protect search patterns.

**Tips**

`grep` searches input line by line. With `-i`, uppercase and lowercase letters are treated alike; by default a pattern can match part of a longer word. Quote the pattern so the shell does not reinterpret it. Decide whether the task means a substring or a whole word, and inspect the actual matching lines rather than counting them.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
ERROR connection lost
Error timeout
```
