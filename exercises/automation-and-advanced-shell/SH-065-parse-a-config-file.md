# SH-065 — Parse a Config File

**Description**

Read a simple `KEY=VALUE` configuration file with comments and blank lines, and print selected settings without executing file contents.

**Tips**

A configuration file should have a documented format, such as simple `KEY=VALUE` pairs. Read lines as text, skip blank lines and comments, split only at the first `=`, and validate recognized keys. Never `source` an untrusted config file, because that would execute arbitrary shell code. Handle missing required settings explicitly.

**What you need to know:** Learn safe line parsing, splitting on the first `=`, and why sourcing untrusted configuration files is unsafe.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
PORT=8080 → port: 8080
```
