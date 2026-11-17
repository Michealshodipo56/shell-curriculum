# SH-011 — Write to a File

**Description**

Write three supplied lines into `message.txt`, replacing any previous contents.

**Tips**

Standard output is the stream where a command normally prints results. `>` redirects that stream into a file and truncates the file first. `printf` is preferable to ambiguous `echo` behavior for controlled text and newlines. Construct the three lines in the required order, redirect once to the destination, and inspect the file afterward to verify exact line breaks.

**What you need to know:** Study standard output and `>` redirection. Use `printf` for predictable line endings; quote strings containing spaces.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
message.txt:
Hello
Shell
World
```
