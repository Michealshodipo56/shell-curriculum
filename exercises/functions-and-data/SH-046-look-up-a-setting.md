# SH-046 — Look Up a Setting

**Description**

Store a small set of key-value settings in an associative array and print the value for a supplied key.

**Tips**

Associative arrays map string keys to values in Bash; they require `declare -A`. Access a key with the appropriate subscript and check whether it exists before assuming a value. Decide how missing keys should be reported. This is Bash-specific, not portable POSIX `sh` syntax.

**What you need to know:** Learn `declare -A`, Bash version requirements, and checking whether a key exists.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
theme → dark
```
