# SH-035 — Count Up

**Description**

Print integers from 1 through a supplied positive limit, one per line.

**Tips**

A C-style loop `for ((i=...; condition; i++))` is one way to count in Bash; `seq` can also generate numbers but is external. Decide whether both endpoints are included and avoid off-by-one errors. Print each value on its own line and verify the first and last numbers.

**What you need to know:** Learn `for` loops and arithmetic loops; validate limits to prevent unbounded output.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
3 → 1
2
3
```
