# SH-019 — Replace Text in a Stream

**Description**

Print a provided file with every occurrence of `dev` replaced by `prod`, leaving the original file unchanged.

**Requirements**

Learn `sed` substitution, the `g` flag, and why printing a transformation differs from in-place editing.

**Tips**

`sed` can transform each input line while printing the result to stdout. A substitution has the shape `s/old/new/g`, where `g` means replace every match on the line rather than only the first. Redirect transformed output somewhere else if needed; do not use in-place editing for a task that requires preserving the original. Verify multiple occurrences on one line.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
input: dev/dev → output: prod/prod
```
