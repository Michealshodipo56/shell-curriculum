# SH-002 — Look Around

**Description**

Display the names of files and directories in the current directory, including hidden entries.

**Requirements**

Explore `ls`, its `-a` option, and why dot-prefixed names are hidden by default. Notice that `.` and `..` are special entries.

**Tips**

By default, `ls` omits entries whose names start with a dot. The `-a` option includes those entries, and `-l` gives permissions and metadata if you need to inspect them. Remember that `.` represents the current directory and `..` its parent; they are not ordinary files you created. Check the command's output against the directory contents rather than inventing filenames.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
.  ..  .config  notes.txt  src
```
