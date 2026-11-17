# SH-020 — Find Files by Name

**Description**

List every `.sh` file beneath a supplied directory, including nested directories.

**Requirements**

Learn `find`, `-type f`, `-name`, and safe handling of spaces in filenames.

**Tips**

`find` walks a directory tree recursively. `-type f` restricts results to regular files, and `-name '*.sh'` matches names ending in `.sh`; quote the pattern so Bash does not expand it before `find` sees it. Start from the supplied root and verify nested results. Treat filenames with spaces as single paths.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./scripts/build.sh
./scripts/tools/check.sh
```
