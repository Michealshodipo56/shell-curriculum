# SH-003 — Travel the Filesystem

**Description**

Navigate from your current directory to a provided directory, then return to the previous location.

**Tips**

`cd` changes the shell's working directory; it does not print the destination by itself. An absolute path begins with `/`, a relative path is interpreted from the current location, `..` moves to the parent, and `~` expands to your home directory. Bash remembers the previous directory in `OLDPWD`, which makes `cd -` useful. Quote paths containing spaces and check your position after each move.

**What you need to know:** Study `cd`, absolute and relative paths, `..`, `~`, and `cd -`. Paths with spaces need quoting.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
before: /home/learner → destination: /tmp/work → back: /home/learner
```
