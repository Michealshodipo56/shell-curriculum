# SH-049 — Handle Optional Flags

**Description**

Support `-v` for verbose mode and `-o FILE` for an output path, rejecting invalid flags.

**Tips**

Flags are optional arguments that modify program behavior, while positional arguments supply primary values. A `while` loop with `case` and `shift`, or `getopts` for short options, can parse them. Validate unknown flags and missing values. Define whether flags may appear in any order before implementing.

**What you need to know:** Learn `getopts`, `OPTARG`, `OPTIND`, and usage messages; test missing option values.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./tool.sh -v -o out.txt → verbose enabled
```

---

## Robust Files and Processes
