# SH-044 — Validate a Number

**Description**

Implement a reusable function that rejects empty or non-integer input before arithmetic.

**Tips**

Validation should happen before arithmetic. A regular expression in `[[ value =~ pattern ]]` can recognize integer syntax; Bash arithmetic comparisons can then enforce ranges. Decide whether negative numbers, leading zeros, or empty strings are allowed. Return an informative error rather than attempting arithmetic on malformed text.

**What you need to know:** Learn `[[ ... =~ ... ]]` with a suitable integer pattern and clear diagnostics to stderr.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
abc → error: expected an integer
```
