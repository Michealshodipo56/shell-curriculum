# SH-025 — Read User Input

**Description**

Prompt for a city and print `You entered: <city>` using the entered value.

**Requirements**

Learn `read -r`, prompting, and why `-r` preserves backslashes. Handle an empty response intentionally.

**Tips**

`read -r` reads a line from standard input into a variable and avoids treating backslashes as escapes. You can print a prompt before reading, or use the prompt option where supported. Empty input is still input; decide what to display for it. Always quote the variable when printing so whitespace is preserved.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
City: Lagos
You entered: Lagos
```
