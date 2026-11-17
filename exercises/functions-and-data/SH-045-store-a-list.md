# SH-045 — Store a List

**Description**

Create a Bash indexed array of supplied names and print the array length and each element.

**Tips**

Bash indexed arrays store multiple values and use zero-based indexes. Assign elements with array syntax, access them with `${array[index]}`, and iterate safely with `"${array[@]}"`. Quoting is essential when an element contains spaces. Do not treat the whole array as one string.

**What you need to know:** Learn `array=(...)`, `${#array[@]}`, and `"${array[@]}"` for preserving whitespace.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
3 names
Ada
Grace
Linus
```
