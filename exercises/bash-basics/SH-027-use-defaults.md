# SH-027 — Use Defaults

**Description**

Print a greeting using the first argument, or `Guest` when no argument is supplied.

**Requirements**

Learn `${1:-Guest}` and how unset/empty values interact with default expansion.

**Tips**

Parameter expansion can supply a fallback when a variable is unset or empty; `${value:-fallback}` is a common form. Distinguish `:-` (use fallback for unset or empty) from `-` (use fallback only when unset). Use the provided argument when present, otherwise select the required default. Quoting prevents word splitting.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./greet.sh → Hello, Guest!
```
