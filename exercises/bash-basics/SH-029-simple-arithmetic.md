# SH-029 — Simple Arithmetic

**Description**

Accept two integers and print their sum, difference, and product.

**Requirements**

Learn Bash arithmetic expansion `$((...))`; validate integer input before calculating.

**Tips**

Bash arithmetic expansion `$(( ... ))` evaluates integer expressions. Inside it, variable names can be used as operands and normal arithmetic operators apply; Bash does not do floating-point arithmetic here. Validate the input before computing, especially when an operand may be empty or nonnumeric. Print the resulting number without extra debugging output.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
8 3 → sum=11 difference=5 product=24
```
