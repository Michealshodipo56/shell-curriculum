# SH-040 — Batch Rename Extensions

**Description**

Rename `.txt` files in a supplied directory to `.bak`, without touching nested directories or overwriting existing files.

**Requirements**

Learn pathname globs, `nullglob` considerations, and collision checks. Work only in the specified directory.

**Tips**

Filename extensions are only conventions; identify the exact suffix before renaming. Shell globs select candidates, and parameter expansion such as `${name%.old}` can remove a matching suffix. Work within the supplied directory, avoid overwriting existing destination files, and handle filenames with spaces safely.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
a.txt → a.bak
```
