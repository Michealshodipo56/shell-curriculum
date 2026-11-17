# SH-008 — Read a Large File

**Description**

Display the first five and last five lines of a provided log file.

**Tips**

`head` reads lines from the beginning of a file and `tail` reads from the end; `-n 5` specifies five lines. You can run them separately and present the results in order. Files shorter than five lines naturally produce fewer lines, so avoid assuming the input has a fixed length. Do not load the entire file into a variable just to show its edges.

**What you need to know:** Learn `head -n`, `tail -n`, and how a line-oriented file differs from a stream of bytes.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
first 5 lines
...
last 5 lines
```
