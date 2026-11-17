# SH-016 — Count Matching Records

**Description**

Print the number of lines containing `failed` in a provided log.

**Tips**

`grep -c` reports how many lines match, not how many occurrences of the word appear. If one line contains the term twice, it still contributes one. A no-match search can return exit status 1 even when the displayed count is zero. Separate the numeric output requirement from the command's status and avoid treating no matches as a crash.

**What you need to know:** Learn `grep -c`, exit statuses for no matches, and the difference between matching lines and occurrences.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
3
```
