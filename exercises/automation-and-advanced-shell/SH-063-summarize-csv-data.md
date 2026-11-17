# SH-063 — Summarize CSV Data

**Description**

From a simple CSV file with `category,amount` rows and no quoted commas, print the sum of amounts per category.

**Tips**

`awk` can split simple delimited rows, keep running totals, and print a summary in an `END` block. Identify the numeric column, skip any header, and validate malformed rows before adding values. Real CSV with quoted delimiters needs a dedicated parser; use only the simplified input promised by the task.

**What you need to know:** Learn `awk -F,`, associative accumulation, numeric conversion, and malformed-record handling.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
food,10
food,5 → food 15
```
