# SH-070 — Process Files Safely

**Description**

Process every `.log` file under a directory, including names with spaces and newlines, and count lines in each.

**Tips**

Shell filenames may contain spaces, tabs, or newlines, so line-delimited `find` output is not universally safe for loops. Prefer `find ... -print0` with `read -r -d ''` or `find ... -exec ... {} +` where appropriate. Quote every path expansion and test with intentionally awkward filenames.

**What you need to know:** Learn `find -print0` and `read -r -d ""`; avoid parsing `ls` output.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
server log.log: 24 lines
```
