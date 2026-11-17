# SH-058 — Check Every Failure

**Description**

Build a script that stops on a failed required step and reports which step failed.

**Tips**

A failed command should not silently allow later destructive work to continue. Check exit statuses with `if command; then ... else ... fi` or explicit `||` handling; `set -e` has exceptions and is not a substitute for deliberate checks. Report the failed operation and return nonzero when the script cannot safely continue.

**What you need to know:** Learn exit-status propagation, `if ! command`, `set -o pipefail`, and limitations of `set -e`; prefer explicit checks where behavior matters.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
error: step "download" failed
```

---

## Automation and Advanced Shell
