# SH-018 — Extract a Column

**Description**

Print the second comma-separated field from each row of a simple CSV file without quoted commas.

**Tips**

`cut` splits a line using a chosen delimiter and selects fields by their 1-based positions. For simple comma-separated data, `-d,` chooses the delimiter and `-f2` selects the second field. This approach does not correctly parse quoted commas in full CSV; the exercise deliberately excludes those. Test a row with multiple columns to confirm which value is extracted.

**What you need to know:** Learn `cut -d, -f2` and its limitations for real CSV containing quoted delimiters.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
Ada
Maya
Linus
```
