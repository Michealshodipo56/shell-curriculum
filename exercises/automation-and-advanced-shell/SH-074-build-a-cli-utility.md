# SH-074 — Build a CLI Utility

**Description**

Create a command-line utility with `--help`, `--version`, a required input path, and an optional output path.

**Requirements**

Learn CLI contracts, argument parsing, useful usage messages, validation, stdout/stderr discipline, and stable exit codes.

**Tips**

A command-line utility needs a stable interface: usage/help text, flags, required arguments, predictable output, and meaningful exit codes. Parse options before performing work, validate inputs, and keep business logic in small functions. Send diagnostics to stderr so stdout remains usable in pipelines. Test help, success, and failure paths.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./tool.sh --help → Usage: tool.sh ...
```
