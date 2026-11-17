# SH-010 — Understand Permissions

**Description**

Inspect a file’s permissions and make a provided script executable by its owner.

**Tips**

Permissions are shown as owner, group, and other read/write/execute bits. On a file, execute permission permits running it as a program; on a directory, it permits traversing it. `chmod u+x` adds execute permission for the owner without changing everyone else's permissions. Compare `ls -l` before and after, and avoid granting unnecessary global write or execute rights.

**What you need to know:** Learn `ls -l`, read/write/execute bits, `chmod u+x`, and why directories need execute permission for traversal.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
-rwxr--r--  ...  hello.sh
```

---

## Streams and Text
