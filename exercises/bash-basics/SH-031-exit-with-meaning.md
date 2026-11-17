# SH-031 — Exit With Meaning

**Description**

Return status 0 when a supplied file exists and nonzero when it does not, printing an appropriate message.

**Tips**

Commands communicate success or failure using an exit status: zero means success and nonzero indicates a problem. `$?` holds the most recent status, but another command can overwrite it immediately. Use `exit N` intentionally and send human-readable errors to stderr. Test both successful and failing invocations.

**What you need to know:** Learn `$?`, `exit`, `test`/`[[ ]]`, and the convention that zero means success.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./exists.sh missing.txt → missing.txt not found (exit 1)
```

---

## Conditions and Loops
