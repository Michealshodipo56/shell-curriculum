# SH-048 — Format a Report

**Description**

Read name-and-score pairs from a simple delimited input file and print an aligned report.

**Requirements**

Learn `printf` field widths, `while IFS= read -r`, and separating parsing from presentation.

**Tips**

`printf` supports controlled field widths and alignment, which makes columns easier to read than concatenating arbitrary spaces. Decide the column names, widths, and row formatting first. Preserve data containing spaces and avoid relying on terminal-specific formatting. Compare the header and rows for consistent alignment.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
NAME       SCORE
Ada        95
```
