# SH-004 — Build a Workspace

**Description**

Create a directory named `practice` containing subdirectories `notes`, `scripts`, and `output`.

**Tips**

`mkdir` creates one directory, while `mkdir -p` can create missing parent directories along a path. Plan the hierarchy before running commands so that `notes`, `scripts`, and `output` are siblings beneath `practice`, not three unrelated folders. Use a listing or `find` to verify the result. Re-running a command with `-p` should not fail just because a directory already exists.

**What you need to know:** Use `mkdir` and `mkdir -p`; understand parent directories and how to verify a directory tree.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
practice/
├── notes/
├── output/
└── scripts/
```
