# SH-014 — Connect Commands

**Description**

Display the number of lines in a provided text file by connecting commands through a pipe.

**Requirements**

Learn `|`, `wc -l`, and how stdout of one process becomes stdin of another. Consider trailing newlines.

**Tips**

A pipe `|` connects one command's stdout to another command's stdin. `wc -l` counts newline characters in the data it receives, so a file without a final newline can be surprising. Choose a command that emits the file's text and pipe it into the counter, or use an equivalent direct input approach if permitted. Keep intermediate data out of unnecessary temporary files.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
12
```
