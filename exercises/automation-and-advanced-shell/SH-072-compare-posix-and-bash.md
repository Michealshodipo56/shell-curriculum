# SH-072 — Compare POSIX and Bash

**Description**

Rewrite a small Bash-only script to work under POSIX `sh`, documenting each feature you replaced.

**Requirements**

Learn `#!/bin/sh`, portable `[ ]`, lack of Bash arrays/`[[ ]]`, and testing with `dash` where available.

**Tips**

POSIX `sh` and Bash overlap but are not identical. Arrays, `[[ ... ]]`, and some parameter expansions are Bash-specific; portable scripts should use POSIX constructs such as `[ ... ]` and compatible loops. Identify the interpreter in the shebang and test under both shells when available. Document features that cannot be used portably.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
sh portable.sh Ada → Hello, Ada!
```
