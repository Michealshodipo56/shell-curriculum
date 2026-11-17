# SH-032 — Positive or Negative

**Description**

Accept an integer and print whether it is positive, negative, or zero.

**Requirements**

Learn `if`, `elif`, `else`, numeric comparisons, and robust integer validation.

**Tips**

Numeric comparisons in Bash use arithmetic contexts such as `(( ... ))`, or test operators like `-gt` and `-lt`. Handle zero separately from positive and negative values. Do not compare numbers lexicographically with string operators. Decide how invalid input is handled before branching.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
-7 → negative
```
