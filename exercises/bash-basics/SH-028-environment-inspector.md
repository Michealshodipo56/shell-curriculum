# SH-028 — Environment Inspector

**Description**

Print the current user, home directory, and shell process ID with labels.

**Tips**

Environment variables are inherited by child processes, while ordinary shell variables are not exported automatically. `printenv` and `env` inspect the environment, and `$HOME`, `$USER`, and `$PATH` are common values. Avoid printing secrets or dumping the full environment in logs. Report only the requested non-sensitive fields.

**What you need to know:** Learn `$HOME`, `$USER`, `$`, and the difference between environment variables and shell variables. `$USER` may not exist everywhere.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
HOME=/home/ada
PID=4123
```
