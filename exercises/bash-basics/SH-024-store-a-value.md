# SH-024 — Store a Value

**Description**

Accept a name in a variable and print a greeting containing that name.

**Requirements**

Learn variable assignment without spaces around `=`, parameter expansion, and double quoting (`"$name"`).

**Tips**

Bash assignments use `name=value` with no spaces around `=`. Refer to the stored value using `$name` or `${name}`. Double quotes around expansions preserve spaces in names, while single quotes prevent expansion. Practice with a one-word name and a multiword value to understand why quoting matters.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
name=Ada → Hello, Ada!
```
