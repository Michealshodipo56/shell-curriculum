# SH-041 — Interactive Menu

**Description**

Present a menu with options to show the date, current directory, or quit; repeat until quit is selected.

**Requirements**

Combine `while`, `case`, `read`, and clear prompts. Handle unknown choices and EOF.

**Tips**

An interactive menu usually displays choices, reads a selection, dispatches with `case`, and repeats until the exit choice is selected. Keep prompting logic separate from each operation. Reject unknown options without terminating unexpectedly. Avoid accidental infinite loops by making the exit path explicit.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
1) Date  2) Directory  3) Quit
Choice: 3
Goodbye
```

---

## Functions and Data
