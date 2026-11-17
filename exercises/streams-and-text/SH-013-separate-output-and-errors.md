# SH-013 — Separate Output and Errors

**Description**

Run a provided failing command and capture standard output and standard error in separate files.

**Tips**

Every process has file descriptors: 0 for standard input, 1 for standard output, and 2 for standard error. Redirect stdout and stderr independently using `1>` and `2>`; the order and placement of redirections matter. A command may write only an error and leave stdout empty. Check both files separately and preserve the command's exit status for diagnosis.

**What you need to know:** Learn file descriptors 1 and 2, `1>`, `2>`, and why diagnostic messages belong on stderr.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
stdout.txt: (empty)
stderr.txt: No such file or directory
```
