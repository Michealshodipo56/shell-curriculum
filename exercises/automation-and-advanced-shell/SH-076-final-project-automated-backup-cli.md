# SH-076 — Final Project: Automated Backup CLI

**Description**

Build a production-minded backup command that validates inputs, creates timestamped archives, supports dry-run and retention options, logs results, and handles failures safely.

**Tips**

Combine the skills learned: parse CLI arguments, validate the source and destination, create an archive, verify it, log the outcome, and apply a safe retention policy. Split responsibilities into functions and stop on errors. Protect against overlapping runs, preserve existing good backups on failure, and test the full workflow in a disposable directory before trusting it.

**What you need to know:** Combine arguments, functions, archives, logging, traps, validation, and safe cleanup. Implement dry-run without changing files; document the CLI and test failure cases.

**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
./backup.sh --source ./project --dest ./backups --keep 3
INFO backup created: backup-20261117-090000.tar.gz
```

---

## Integration notes

The agent should preserve exercise IDs and order, convert each task into the application’s exercise schema, create isolated fixtures for file-based tasks, and assess behavior rather than hard-coded incidental values. For tasks with interactive input, provide stdin fixtures; for filesystem tasks, inspect generated files and permissions. Prefer explicit deterministic test inputs. Do not reveal full reference solutions in the learner-facing tips.
