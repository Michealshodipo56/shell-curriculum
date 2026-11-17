# SH-039 — Process Every Argument

**Description**

Print each supplied command-line argument on its own numbered line, preserving spaces.

**Requirements**

Learn `"$@"` versus `"$*"`, loop counters, and correct quoting.

**Tips**

`"$@"` expands each positional argument as a separate preserved item, including arguments containing spaces. By contrast, unquoted `$*` or `$@` can split them unexpectedly. Iterate over the arguments without losing their boundaries. Test with no arguments and with one argument containing spaces.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./args.sh "red apple" pear → 1: red apple
2: pear
```
