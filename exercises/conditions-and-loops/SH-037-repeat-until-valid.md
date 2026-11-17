# SH-037 — Repeat Until Valid

**Description**

Keep prompting for a nonempty username until the user provides one, then print it.

**Tips**

A `while` loop repeats while its condition is true; an `until` loop repeats until a condition becomes true. Put the input prompt and validation inside the loop, and ensure each iteration can change the condition so the script cannot become stuck. Define what counts as valid before writing the loop.

**What you need to know:** Learn `while`, condition negation, `read -r`, and how to stop cleanly on end-of-file rather than looping forever.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
Username: 
Username: ada
Accepted: ada
```
