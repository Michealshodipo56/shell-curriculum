# SH-009 — Find Your Commands

**Description**

Determine where `bash`, `grep`, and `awk` are found and display their available help information.

**Requirements**

Learn `command -v`, `type`, `--help`, `man`, and shell builtins versus external executables.

**Tips**

Shell commands can be builtins, functions, aliases, or external programs. `type` explains what Bash will execute, while `command -v` reports how a command resolves on `PATH`. Many external programs support `--help`; `man` opens longer manual pages when installed. Check all three requested commands and do not assume executable locations are identical across machines.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
bash: /usr/bin/bash (path may vary)
```
