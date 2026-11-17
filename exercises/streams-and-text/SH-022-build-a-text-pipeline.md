# SH-022 — Build a Text Pipeline

**Description**

From a provided access log, output the five most frequent IP addresses in descending frequency.

**Tips**

Break the pipeline into small stages: identify the IP field, extract it, sort identical addresses together, count repeated lines, then sort by the numeric count in descending order and keep the top five. `awk` is useful for whitespace-delimited fields, `uniq -c` counts adjacent duplicates, and `sort -nr` sorts counts. Inspect intermediate output when results look wrong.

**What you need to know:** Combine field extraction, sorting, counting, and numeric reverse sorting. `awk` can select fields; `uniq -c` counts adjacent entries.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
12 192.0.2.4
8 198.51.100.9
```

---

## Bash Basics
