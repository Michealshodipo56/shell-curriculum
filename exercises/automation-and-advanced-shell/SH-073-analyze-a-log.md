# SH-073 — Analyze a Log

**Description**

Produce a summary of total records, errors, and the three most common error messages from a supplied structured log.

**Tips**

Log analysis begins with defining the record format and the fields that matter. Filter relevant lines, extract timestamps or statuses, aggregate counts, and sort the summary. Build the pipeline in stages and check sample records to avoid counting malformed entries. Make the final report deterministic for the same input.

**What you need to know:** Combine pipelines, `awk`, `sort`, `uniq`, and explicit parsing assumptions. Keep output deterministic for automated assessment.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
total=100
errors=8
top_error=timeout (4)
```
