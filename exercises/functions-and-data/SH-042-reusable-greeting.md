# SH-042 — Reusable Greeting

**Description**

Define a function that accepts a name and prints a greeting; invoke it for each supplied argument.

**Tips**

A Bash function groups commands under a reusable name and runs in the current shell context. Function parameters use `$1`, `$2`, and so on, independent of the script's outer arguments while the function runs. Call the function with different inputs and quote the parameters to preserve spaces.

**What you need to know:** Learn Bash function syntax, local positional parameters, and `local` variables.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
Ada Maya → Hello, Ada!
Hello, Maya!
```
