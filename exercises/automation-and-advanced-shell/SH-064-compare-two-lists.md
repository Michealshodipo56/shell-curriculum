# SH-064 — Compare Two Lists

**Description**

Print values that occur in the first newline-delimited file but not the second, ignoring duplicate lines.

**Tips**

`comm` compares two sorted files line by line, while `sort` and `uniq` can normalize lists first. Decide whether the output should be the intersection, items unique to one list, or both differences. Remove duplicate entries before comparison if the task treats each item as a set member. Preserve a deterministic output order.

**What you need to know:** Learn `sort -u` and `comm -23` with sorted inputs; decide whether comparison is case-sensitive.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
A: ada, maya; B: maya → ada
```
