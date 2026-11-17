# SH-034 — Choose an Operation

**Description**

Accept an operation (`add`, `subtract`, `multiply`) and two integers, then print the result.

**Tips**

`case` is useful when one input can select among several known commands or labels. Each pattern has a branch and an unmatched fallback can use `*`. Keep the branch bodies focused on their operations and reject unsupported choices. Avoid using `eval` to execute raw user input.

**What you need to know:** Learn `case ... in ... esac`, default branches, and argument checking.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
multiply 4 6 → 24
```
