# SH-001 — Where Am I?

**Description**

Print the absolute path of the current working directory.

**Requirements**

A shell maintains a working directory. Learn what an absolute path is and how `pwd` reports it; do not confuse the home directory with the current directory.

**Tips**

Your terminal always has a current directory, even when the prompt does not show it. `pwd` asks the shell to print that location. An absolute path starts at `/`, whereas a relative path starts from wherever you currently are. Run the directory-reporting command without assuming you are in your home folder; verify by changing into a different directory and checking again.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
/home/learner/projects
```
