# SH-017 — Sort and Deduplicate

**Description**

Produce a sorted list of distinct usernames from a provided one-name-per-line file.

**Tips**

`sort` orders lines; `uniq` removes repeated adjacent lines. If duplicates are separated in the original input, `uniq` alone will miss them. Sort first, then remove duplicates, or use a suitable combined option. Decide whether case differences should count as distinct usernames, and ensure the output contains one username per line.

**What you need to know:** Learn `sort`, `uniq`, and why adjacent duplicate removal generally requires sorting first.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
ada
linus
maya
```
