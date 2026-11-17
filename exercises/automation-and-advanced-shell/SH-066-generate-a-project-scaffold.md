# SH-066 — Generate a Project Scaffold

**Description**

Create a standard project directory structure from a supplied project name, refusing to overwrite an existing project.

**Requirements**

Learn `mkdir -p`, templates, path validation, and idempotency.

**Tips**

A scaffold generator creates a predictable directory and file layout from a project name. Validate names to avoid path traversal, create parents with `mkdir -p`, and write template files using a here-document or `printf`. Decide whether existing files should be preserved. Test the generated tree rather than only the generator's output message.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
demo/
├── README.md
├── src/
└── tests/
```
