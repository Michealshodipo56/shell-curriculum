# SH-023 — Your First Script

**Description**

Create an executable Bash script that prints `Hello, Shell!` when invoked.

**Requirements**

Learn the `#!/usr/bin/env bash` shebang, executable permissions, and the difference between `bash script.sh` and `./script.sh`.

**Tips**

A shebang such as `#!/usr/bin/env bash` tells the operating system which interpreter to use when the file is executed directly. A script is plain text containing shell commands. `bash file.sh` runs it through Bash even without executable permission, while `./file.sh` requires appropriate permissions. Make the greeting exact, including punctuation and newline.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
Hello, Shell!
```
