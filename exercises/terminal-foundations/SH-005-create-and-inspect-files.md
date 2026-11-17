# SH-005 — Create and Inspect Files

**Description**

Create an empty `notes/todo.txt`, then display its contents and file metadata.

**Tips**

`touch` creates a file if absent, but can also update timestamps on an existing file. `cat` prints contents, so an empty file produces no visible text; that is not an error. `stat` exposes file size and metadata. Distinguish checking that a path exists from checking that its byte size is zero; verify both before considering the task complete.

**What you need to know:** Learn `touch`, `cat`, `stat`, and the difference between a file existing and having content.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
notes/todo.txt exists; its size is 0 bytes
```
