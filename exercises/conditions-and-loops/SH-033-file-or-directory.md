# SH-033 — File or Directory?

**Description**

Accept a path and report whether it names a regular file, directory, or missing/other path.

**Requirements**

Learn `[[ -f ... ]]`, `[[ -d ... ]]`, and `[[ -e ... ]]`; symbolic links may need special consideration.

**Tips**

File tests such as `-f`, `-d`, and `-e` answer different questions: regular file, directory, and existence. Put path variables in quotes, particularly when paths contain spaces. Check the requested categories in an order that avoids misclassifying directories as files. Handle missing paths explicitly.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./notes → directory
```
