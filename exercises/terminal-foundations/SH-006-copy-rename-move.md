# SH-006 — Copy, Rename, Move

**Description**

Copy a provided `draft.txt` to `notes/draft.txt`, rename the copy to `final.txt`, and move it into `output`.

**Tips**

`cp` duplicates data and leaves the source in place; `mv` relocates or renames a path. Both take a source followed by a destination. Think through each intermediate location: copy into `notes`, rename only that copy, then move it into `output`. A destination that already exists may be overwritten, so work only inside the exercise workspace and inspect the final locations.

**What you need to know:** Learn `cp` and `mv`, source/destination ordering, and why overwriting existing files can lose data.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
output/final.txt exists; original draft.txt remains
```
