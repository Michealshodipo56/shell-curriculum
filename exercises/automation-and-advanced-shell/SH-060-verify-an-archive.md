# SH-060 — Verify an Archive

**Description**

List the contents of a supplied tar archive and reject archives containing absolute paths or `..` traversal components before extraction.

**Tips**

Archive creation is not proof that the contents are correct. `tar -tf` lists members without extracting them, and a temporary extraction directory can support deeper checks. Compare expected relative paths and file contents while guarding against unsafe paths. Leave the original source untouched.

**What you need to know:** Learn `tar -tf`, archive path traversal risks, and why inspection must precede extraction.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
archive accepted: 4 entries
```
