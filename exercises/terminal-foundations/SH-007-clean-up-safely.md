# SH-007 — Clean Up Safely

**Description**

Remove only the supplied temporary file and an empty temporary directory without deleting any other content.

**Requirements**

Learn `rm`, `rmdir`, and why recursive deletion is dangerous. Inspect the target first; avoid wildcard deletion in unfamiliar paths.

**Tips**

`rm` deletes files without moving them to a recycle bin; `rmdir` removes directories only when they are empty. Before deleting, inspect the exact target and confirm it lies inside the provided temporary workspace. Avoid broad glob patterns and recursive deletion for this exercise. After removal, confirm the requested paths are gone while neighboring files still exist.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
temporary file removed; unrelated files unchanged
```
