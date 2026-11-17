# Gauntlex Master Shell Curriculum

> **Track:** Shell & Bash · **Primary shell:** Bash · **Progression:** Beginner → Advanced · **Format:** One Markdown file, ordered exercises

## Purpose

A sequential, hands-on Shell curriculum for Gauntlex. Each exercise is a distinct learning milestone rather than a copy of an upstream assignment. Exercises deliberately combine overlapping skills into progressively more demanding tasks. Bash is the default interpreter; POSIX portability is introduced explicitly near the end.

## Source inspiration and attribution

- [Learn Linux with Ease](https://github.com/akintunero/learn-linux-with-ease)
- [The Complete Bash Scripting Course](https://github.com/bahamas10/bash-course)
- [The Bash Command Line — Kristian Rother](https://github.com/krother/bash_tutorial)
- [Practice Shell Challenges — LabEx](https://github.com/labex-labs/shell-practice-challenges)
- [Shell Scripting — From Beginner to Automation](https://github.com/kcommit/shell-scripting)

**Provenance limitation:** This is an original, topic-level synthesis inspired by the five selected resources, not a verified file-by-file extraction or a claim that every upstream exercise was reviewed. The assignments and explanations below are newly written. Before importing third-party source text, code, or tests, inspect each repository's current license and attribution requirements. No upstream text or tests are reproduced here.

## Gauntlex integration contract

- **Canonical order:** Exercise IDs `SH-001` onward are stable and sequential; unlock the next exercise after the previous one passes assessment.
- **Description:** The assignment and expected behavior, without a solution.
- **Tips:** Teaches the required concepts, tools, constraints, and useful approaches, but does not contain a complete solution.
- **Example:** Illustrative terminal interaction or expected output; variable paths, timestamps, and PIDs are examples, not fixed assertions.
- **Assessment:** Have the integration agent derive executable checks from the description and edge cases; examples are not comprehensive test specifications.
- **Runtime:** Linux with Bash and standard GNU/coreutils-style commands unless otherwise stated. External dependencies are called out in tips.
- **Safety:** All filesystem tasks must run in an isolated workspace. Do not execute destructive tasks on user data.
- **Parsing:** Every task begins with a level-three heading of the form `### SH-NNN — Title` and contains exactly `**Description**`, `**Tips**`, and `**Example**` sections.

## Curriculum map

- **Terminal Foundations:** 10 exercises
- **Streams and Text:** 12 exercises
- **Bash Basics:** 9 exercises
- **Conditions and Loops:** 10 exercises
- **Functions and Data:** 8 exercises
- **Robust Files and Processes:** 9 exercises
- **Automation and Advanced Shell:** 18 exercises

**Total: 76 exercises.**

---

## Terminal Foundations

### SH-001 — Where Am I?

**Description**

Print the absolute path of the current working directory.

**Tips**

A shell maintains a working directory. Learn what an absolute path is and how `pwd` reports it; do not confuse the home directory with the current directory.

**Example**

```text
/home/learner/projects
```

### SH-002 — Look Around

**Description**

Display the names of files and directories in the current directory, including hidden entries.

**Tips**

Explore `ls`, its `-a` option, and why dot-prefixed names are hidden by default. Notice that `.` and `..` are special entries.

**Example**

```text
.  ..  .config  notes.txt  src
```

### SH-003 — Travel the Filesystem

**Description**

Navigate from your current directory to a provided directory, then return to the previous location.

**Tips**

Study `cd`, absolute and relative paths, `..`, `~`, and `cd -`. Paths with spaces need quoting.

**Example**

```text
before: /home/learner → destination: /tmp/work → back: /home/learner
```

### SH-004 — Build a Workspace

**Description**

Create a directory named `practice` containing subdirectories `notes`, `scripts`, and `output`.

**Tips**

Use `mkdir` and `mkdir -p`; understand parent directories and how to verify a directory tree.

**Example**

```text
practice/
├── notes/
├── output/
└── scripts/
```

### SH-005 — Create and Inspect Files

**Description**

Create an empty `notes/todo.txt`, then display its contents and file metadata.

**Tips**

Learn `touch`, `cat`, `stat`, and the difference between a file existing and having content.

**Example**

```text
notes/todo.txt exists; its size is 0 bytes
```

### SH-006 — Copy, Rename, Move

**Description**

Copy a provided `draft.txt` to `notes/draft.txt`, rename the copy to `final.txt`, and move it into `output`.

**Tips**

Learn `cp` and `mv`, source/destination ordering, and why overwriting existing files can lose data.

**Example**

```text
output/final.txt exists; original draft.txt remains
```

### SH-007 — Clean Up Safely

**Description**

Remove only the supplied temporary file and an empty temporary directory without deleting any other content.

**Tips**

Learn `rm`, `rmdir`, and why recursive deletion is dangerous. Inspect the target first; avoid wildcard deletion in unfamiliar paths.

**Example**

```text
temporary file removed; unrelated files unchanged
```

### SH-008 — Read a Large File

**Description**

Display the first five and last five lines of a provided log file.

**Tips**

Learn `head -n`, `tail -n`, and how a line-oriented file differs from a stream of bytes.

**Example**

```text
first 5 lines
...
last 5 lines
```

### SH-009 — Find Your Commands

**Description**

Determine where `bash`, `grep`, and `awk` are found and display their available help information.

**Tips**

Learn `command -v`, `type`, `--help`, `man`, and shell builtins versus external executables.

**Example**

```text
bash: /usr/bin/bash (path may vary)
```

### SH-010 — Understand Permissions

**Description**

Inspect a file’s permissions and make a provided script executable by its owner.

**Tips**

Learn `ls -l`, read/write/execute bits, `chmod u+x`, and why directories need execute permission for traversal.

**Example**

```text
-rwxr--r--  ...  hello.sh
```

---

## Streams and Text

### SH-011 — Write to a File

**Description**

Write three supplied lines into `message.txt`, replacing any previous contents.

**Tips**

Study standard output and `>` redirection. Use `printf` for predictable line endings; quote strings containing spaces.

**Example**

```text
message.txt:
Hello
Shell
World
```

### SH-012 — Append an Activity Log

**Description**

Add a new timestamped message to `activity.log` without deleting existing entries.

**Tips**

Study `>>`, the `date` command, and the difference between overwrite and append. The timestamp format should be documented.

**Example**

```text
2026-11-17 09:00:00 started
```

### SH-013 — Separate Output and Errors

**Description**

Run a provided failing command and capture standard output and standard error in separate files.

**Tips**

Learn file descriptors 1 and 2, `1>`, `2>`, and why diagnostic messages belong on stderr.

**Example**

```text
stdout.txt: (empty)
stderr.txt: No such file or directory
```

### SH-014 — Connect Commands

**Description**

Display the number of lines in a provided text file by connecting commands through a pipe.

**Tips**

Learn `|`, `wc -l`, and how stdout of one process becomes stdin of another. Consider trailing newlines.

**Example**

```text
12
```

### SH-015 — Search for a Word

**Description**

Print every line in a provided file containing the word `error`, ignoring letter case.

**Tips**

Learn `grep -i`, matching substrings, and why quotes help protect search patterns.

**Example**

```text
ERROR connection lost
Error timeout
```

### SH-016 — Count Matching Records

**Description**

Print the number of lines containing `failed` in a provided log.

**Tips**

Learn `grep -c`, exit statuses for no matches, and the difference between matching lines and occurrences.

**Example**

```text
3
```

### SH-017 — Sort and Deduplicate

**Description**

Produce a sorted list of distinct usernames from a provided one-name-per-line file.

**Tips**

Learn `sort`, `uniq`, and why adjacent duplicate removal generally requires sorting first.

**Example**

```text
ada
linus
maya
```

### SH-018 — Extract a Column

**Description**

Print the second comma-separated field from each row of a simple CSV file without quoted commas.

**Tips**

Learn `cut -d, -f2` and its limitations for real CSV containing quoted delimiters.

**Example**

```text
Ada
Maya
Linus
```

### SH-019 — Replace Text in a Stream

**Description**

Print a provided file with every occurrence of `dev` replaced by `prod`, leaving the original file unchanged.

**Tips**

Learn `sed` substitution, the `g` flag, and why printing a transformation differs from in-place editing.

**Example**

```text
input: dev/dev → output: prod/prod
```

### SH-020 — Find Files by Name

**Description**

List every `.sh` file beneath a supplied directory, including nested directories.

**Tips**

Learn `find`, `-type f`, `-name`, and safe handling of spaces in filenames.

**Example**

```text
./scripts/build.sh
./scripts/tools/check.sh
```

### SH-021 — Inspect Disk Usage

**Description**

Report the human-readable total size of a supplied directory and the free space on its filesystem.

**Tips**

Learn `du -sh` and `df -h`; explain used directory space versus available filesystem capacity.

**Example**

```text
directory: 24K; filesystem available: 8.2G
```

### SH-022 — Build a Text Pipeline

**Description**

From a provided access log, output the five most frequent IP addresses in descending frequency.

**Tips**

Combine field extraction, sorting, counting, and numeric reverse sorting. `awk` can select fields; `uniq -c` counts adjacent entries.

**Example**

```text
12 192.0.2.4
8 198.51.100.9
```

---

## Bash Basics

### SH-023 — Your First Script

**Description**

Create an executable Bash script that prints `Hello, Shell!` when invoked.

**Tips**

Learn the `#!/usr/bin/env bash` shebang, executable permissions, and the difference between `bash script.sh` and `./script.sh`.

**Example**

```text
Hello, Shell!
```

### SH-024 — Store a Value

**Description**

Accept a name in a variable and print a greeting containing that name.

**Tips**

Learn variable assignment without spaces around `=`, parameter expansion, and double quoting (`"$name"`).

**Example**

```text
name=Ada → Hello, Ada!
```

### SH-025 — Read User Input

**Description**

Prompt for a city and print `You entered: <city>` using the entered value.

**Tips**

Learn `read -r`, prompting, and why `-r` preserves backslashes. Handle an empty response intentionally.

**Example**

```text
City: Lagos
You entered: Lagos
```

### SH-026 — Accept Positional Arguments

**Description**

Write a script that accepts a first name and surname as two command-line arguments and prints them together.

**Tips**

Learn `$1`, `$2`, `$#`, and argument validation. Always quote positional expansions.

**Example**

```text
./full-name.sh Ada Lovelace → Ada Lovelace
```

### SH-027 — Use Defaults

**Description**

Print a greeting using the first argument, or `Guest` when no argument is supplied.

**Tips**

Learn `${1:-Guest}` and how unset/empty values interact with default expansion.

**Example**

```text
./greet.sh → Hello, Guest!
```

### SH-028 — Environment Inspector

**Description**

Print the current user, home directory, and shell process ID with labels.

**Tips**

Learn `$HOME`, `$USER`, `$$`, and the difference between environment variables and shell variables. `$USER` may not exist everywhere.

**Example**

```text
HOME=/home/ada
PID=4123
```

### SH-029 — Simple Arithmetic

**Description**

Accept two integers and print their sum, difference, and product.

**Tips**

Learn Bash arithmetic expansion `$((...))`; validate integer input before calculating.

**Example**

```text
8 3 → sum=11 difference=5 product=24
```

### SH-030 — Quote It Correctly

**Description**

Write a script that creates a file using a filename supplied as an argument, including filenames containing spaces.

**Tips**

Learn double quoting, word splitting, glob expansion, and safe argument handling; never build command strings using `eval`.

**Example**

```text
./make-file.sh "my notes.txt" → my notes.txt created
```

### SH-031 — Exit With Meaning

**Description**

Return status 0 when a supplied file exists and nonzero when it does not, printing an appropriate message.

**Tips**

Learn `$?`, `exit`, `test`/`[[ ]]`, and the convention that zero means success.

**Example**

```text
./exists.sh missing.txt → missing.txt not found (exit 1)
```

---

## Conditions and Loops

### SH-032 — Positive or Negative

**Description**

Accept an integer and print whether it is positive, negative, or zero.

**Tips**

Learn `if`, `elif`, `else`, numeric comparisons, and robust integer validation.

**Example**

```text
-7 → negative
```

### SH-033 — File or Directory?

**Description**

Accept a path and report whether it names a regular file, directory, or missing/other path.

**Tips**

Learn `[[ -f ... ]]`, `[[ -d ... ]]`, and `[[ -e ... ]]`; symbolic links may need special consideration.

**Example**

```text
./notes → directory
```

### SH-034 — Choose an Operation

**Description**

Accept an operation (`add`, `subtract`, `multiply`) and two integers, then print the result.

**Tips**

Learn `case ... in ... esac`, default branches, and argument checking.

**Example**

```text
multiply 4 6 → 24
```

### SH-035 — Count Up

**Description**

Print integers from 1 through a supplied positive limit, one per line.

**Tips**

Learn `for` loops and arithmetic loops; validate limits to prevent unbounded output.

**Example**

```text
3 → 1
2
3
```

### SH-036 — Even Numbers Only

**Description**

Print every even number from 2 through a supplied nonnegative upper bound.

**Tips**

Learn modulo `%`, arithmetic tests, and loops; consider what happens when the bound is below 2.

**Example**

```text
7 → 2 4 6
```

### SH-037 — Repeat Until Valid

**Description**

Keep prompting for a nonempty username until the user provides one, then print it.

**Tips**

Learn `while`, condition negation, `read -r`, and how to stop cleanly on end-of-file rather than looping forever.

**Example**

```text
Username: 
Username: ada
Accepted: ada
```

### SH-038 — Sum a Sequence

**Description**

Accept a positive integer N and print the sum of integers from 1 through N.

**Tips**

Use a loop with an accumulator; learn variable updates and Bash integer arithmetic.

**Example**

```text
5 → 15
```

### SH-039 — Process Every Argument

**Description**

Print each supplied command-line argument on its own numbered line, preserving spaces.

**Tips**

Learn `"$@"` versus `"$*"`, loop counters, and correct quoting.

**Example**

```text
./args.sh "red apple" pear → 1: red apple
2: pear
```

### SH-040 — Batch Rename Extensions

**Description**

Rename `.txt` files in a supplied directory to `.bak`, without touching nested directories or overwriting existing files.

**Tips**

Learn pathname globs, `nullglob` considerations, and collision checks. Work only in the specified directory.

**Example**

```text
a.txt → a.bak
```

### SH-041 — Interactive Menu

**Description**

Present a menu with options to show the date, current directory, or quit; repeat until quit is selected.

**Tips**

Combine `while`, `case`, `read`, and clear prompts. Handle unknown choices and EOF.

**Example**

```text
1) Date  2) Directory  3) Quit
Choice: 3
Goodbye
```

---

## Functions and Data

### SH-042 — Reusable Greeting

**Description**

Define a function that accepts a name and prints a greeting; invoke it for each supplied argument.

**Tips**

Learn Bash function syntax, local positional parameters, and `local` variables.

**Example**

```text
Ada Maya → Hello, Ada!
Hello, Maya!
```

### SH-043 — Return Status, Print Data

**Description**

Define a function that checks whether a supplied path is readable and use its exit status to print a result.

**Tips**

Learn that `return` communicates an integer status (0–255), while stdout carries text results.

**Example**

```text
notes.txt → readable
```

### SH-044 — Validate a Number

**Description**

Implement a reusable function that rejects empty or non-integer input before arithmetic.

**Tips**

Learn `[[ ... =~ ... ]]` with a suitable integer pattern and clear diagnostics to stderr.

**Example**

```text
abc → error: expected an integer
```

### SH-045 — Store a List

**Description**

Create a Bash indexed array of supplied names and print the array length and each element.

**Tips**

Learn `array=(...)`, `${#array[@]}`, and `"${array[@]}"` for preserving whitespace.

**Example**

```text
3 names
Ada
Grace
Linus
```

### SH-046 — Look Up a Setting

**Description**

Store a small set of key-value settings in an associative array and print the value for a supplied key.

**Tips**

Learn `declare -A`, Bash version requirements, and checking whether a key exists.

**Example**

```text
theme → dark
```

### SH-047 — Build a Library

**Description**

Move reusable validation and formatting functions into `lib.sh` and load them from a second script.

**Tips**

Learn `source`/`.` and how sourcing executes code in the current shell; resolve library paths relative to the script.

**Example**

```text
./main.sh 12 → valid: 12
```

### SH-048 — Format a Report

**Description**

Read name-and-score pairs from a simple delimited input file and print an aligned report.

**Tips**

Learn `printf` field widths, `while IFS= read -r`, and separating parsing from presentation.

**Example**

```text
NAME       SCORE
Ada        95
```

### SH-049 — Handle Optional Flags

**Description**

Support `-v` for verbose mode and `-o FILE` for an output path, rejecting invalid flags.

**Tips**

Learn `getopts`, `OPTARG`, `OPTIND`, and usage messages; test missing option values.

**Example**

```text
./tool.sh -v -o out.txt → verbose enabled
```

---

## Robust Files and Processes

### SH-050 — Read Every Line

**Description**

Print numbered lines from a supplied text file, preserving leading spaces and backslashes.

**Tips**

Use `while IFS= read -r line || [[ -n $line ]]` to handle the final line without a newline.

**Example**

```text
1: alpha
2: beta
```

### SH-051 — Find Empty Files

**Description**

List regular files of size zero beneath a provided directory.

**Tips**

Learn `find -type f -empty` and distinguish empty files from empty directories.

**Example**

```text
./data/empty.txt
```

### SH-052 — Safe Temporary Workspace

**Description**

Create a temporary directory, write an intermediate file, and remove the temporary directory on normal exit or interruption.

**Tips**

Learn `mktemp -d`, `trap`, safe quoting, and cleanup for EXIT; consider signal behavior.

**Example**

```text
temporary work completed; no temporary directory remains
```

### SH-053 — Check a Dependency

**Description**

Verify that a required external command is installed before running a task; otherwise print a useful error and exit nonzero.

**Tips**

Learn `command -v`, stderr messages, and why explicit dependency checks improve portability.

**Example**

```text
error: required command jq is missing
```

### SH-054 — Understand Process IDs

**Description**

Start a short-lived background command, print its PID, wait for it, and report its exit status.

**Tips**

Learn `&`, `$!`, `wait`, and the difference between parent and child processes.

**Example**

```text
started PID 1234
finished status 0
```

### SH-055 — Stop Gracefully

**Description**

Write a long-running script that handles SIGINT and SIGTERM by cleaning up and exiting.

**Tips**

Learn `trap`, signals, interruption, and idempotent cleanup. Do not assume SIGKILL can be trapped.

**Example**

```text
received termination signal; cleaned up
```

### SH-056 — Prevent Concurrent Runs

**Description**

Ensure two instances of a script cannot modify the same output at once.

**Tips**

Learn advisory locking with `flock` on Linux or an atomic-directory strategy; explain cleanup and stale-lock concerns.

**Example**

```text
second run → already running (exit 1)
```

### SH-057 — Log With Levels

**Description**

Write reusable logging functions for INFO, WARN, and ERROR with timestamps, sending errors to stderr.

**Tips**

Learn `printf`, date formatting, output streams, and why structured, consistent logs help debugging.

**Example**

```text
2026-11-17T09:00:00 INFO started
```

### SH-058 — Check Every Failure

**Description**

Build a script that stops on a failed required step and reports which step failed.

**Tips**

Learn exit-status propagation, `if ! command`, `set -o pipefail`, and limitations of `set -e`; prefer explicit checks where behavior matters.

**Example**

```text
error: step "download" failed
```

---

## Automation and Advanced Shell

### SH-059 — Archive a Directory

**Description**

Create a compressed `.tar.gz` archive of a supplied directory with a predictable output filename.

**Tips**

Learn `tar -czf`, relative archive paths, quoting, and how to inspect an archive before trusting it.

**Example**

```text
project/ → project.tar.gz
```

### SH-060 — Verify an Archive

**Description**

List the contents of a supplied tar archive and reject archives containing absolute paths or `..` traversal components before extraction.

**Tips**

Learn `tar -tf`, archive path traversal risks, and why inspection must precede extraction.

**Example**

```text
archive accepted: 4 entries
```

### SH-061 — Backup With Rotation

**Description**

Back up a specified directory to timestamped archives and retain only the newest N backups.

**Tips**

Learn timestamp naming, sorting, retention rules, and safe deletion restricted to a dedicated backup directory.

**Example**

```text
backup-20261117-090000.tar.gz created; 3 retained
```

### SH-062 — Monitor a Log

**Description**

Follow newly appended lines in a log and print only those matching a supplied keyword until interrupted.

**Tips**

Learn `tail -f` or `tail -F`, pipes, buffering, and graceful termination.

**Example**

```text
new line: ERROR database unavailable
```

### SH-063 — Summarize CSV Data

**Description**

From a simple CSV file with `category,amount` rows and no quoted commas, print the sum of amounts per category.

**Tips**

Learn `awk -F,`, associative accumulation, numeric conversion, and malformed-record handling.

**Example**

```text
food,10
food,5 → food 15
```

### SH-064 — Compare Two Lists

**Description**

Print values that occur in the first newline-delimited file but not the second, ignoring duplicate lines.

**Tips**

Learn `sort -u` and `comm -23` with sorted inputs; decide whether comparison is case-sensitive.

**Example**

```text
A: ada, maya; B: maya → ada
```

### SH-065 — Parse a Config File

**Description**

Read a simple `KEY=VALUE` configuration file with comments and blank lines, and print selected settings without executing file contents.

**Tips**

Learn safe line parsing, splitting on the first `=`, and why sourcing untrusted configuration files is unsafe.

**Example**

```text
PORT=8080 → port: 8080
```

### SH-066 — Generate a Project Scaffold

**Description**

Create a standard project directory structure from a supplied project name, refusing to overwrite an existing project.

**Tips**

Learn `mkdir -p`, templates, path validation, and idempotency.

**Example**

```text
demo/
├── README.md
├── src/
└── tests/
```

### SH-067 — Schedule a Script

**Description**

Write a script suitable for scheduled execution and document a cron entry that runs it daily at 02:00.

**Tips**

Learn cron’s five time fields, minimal environment, absolute paths, output redirection, and timezone considerations.

**Example**

```text
0 2 * * * /absolute/path/job.sh
```

### SH-068 — Check Service Health

**Description**

Accept a URL, make an HTTP request, and report whether it returns a successful 2xx status.

**Tips**

Learn `curl -sS -o /dev/null -w`, timeouts, network failure handling, and the distinction between transport errors and HTTP status codes.

**Example**

```text
https://example.org → healthy (200)
```

### SH-069 — Retry a Flaky Command

**Description**

Run a supplied command up to a configurable maximum number of attempts, waiting between failures and stopping immediately on success.

**Tips**

Learn retries, exit statuses, bounded loops, delays, and why some operations are unsafe to retry.

**Example**

```text
attempt 1 failed
attempt 2 succeeded
```

### SH-070 — Process Files Safely

**Description**

Process every `.log` file under a directory, including names with spaces and newlines, and count lines in each.

**Tips**

Learn `find -print0` and `read -r -d ""`; avoid parsing `ls` output.

**Example**

```text
server log.log: 24 lines
```

### SH-071 — Use a Subshell

**Description**

Run a command in a supplied directory without changing the caller’s working directory.

**Tips**

Learn `( ... )` subshell grouping and how directory changes and variable assignments are isolated.

**Example**

```text
before=/home/ada
inside=/tmp
after=/home/ada
```

### SH-072 — Compare POSIX and Bash

**Description**

Rewrite a small Bash-only script to work under POSIX `sh`, documenting each feature you replaced.

**Tips**

Learn `#!/bin/sh`, portable `[ ]`, lack of Bash arrays/`[[ ]]`, and testing with `dash` where available.

**Example**

```text
sh portable.sh Ada → Hello, Ada!
```

### SH-073 — Analyze a Log

**Description**

Produce a summary of total records, errors, and the three most common error messages from a supplied structured log.

**Tips**

Combine pipelines, `awk`, `sort`, `uniq`, and explicit parsing assumptions. Keep output deterministic for automated assessment.

**Example**

```text
total=100
errors=8
top_error=timeout (4)
```

### SH-074 — Build a CLI Utility

**Description**

Create a command-line utility with `--help`, `--version`, a required input path, and an optional output path.

**Tips**

Learn CLI contracts, argument parsing, useful usage messages, validation, stdout/stderr discipline, and stable exit codes.

**Example**

```text
./tool.sh --help → Usage: tool.sh ...
```

### SH-075 — Test a Shell Script

**Description**

Write a shell-based test harness that runs a supplied utility with valid and invalid inputs and checks output and exit status.

**Tips**

Learn temporary fixtures, output capture, expected statuses, and why tests should isolate their working directory.

**Example**

```text
PASS valid input
PASS missing file
2 tests passed
```

### SH-076 — Final Project: Automated Backup CLI

**Description**

Build a production-minded backup command that validates inputs, creates timestamped archives, supports dry-run and retention options, logs results, and handles failures safely.

**Tips**

Combine arguments, functions, archives, logging, traps, validation, and safe cleanup. Implement dry-run without changing files; document the CLI and test failure cases.

**Example**

```text
./backup.sh --source ./project --dest ./backups --keep 3
INFO backup created: backup-20261117-090000.tar.gz
```

---

## Integration notes

The agent should preserve exercise IDs and order, convert each task into the application’s exercise schema, create isolated fixtures for file-based tasks, and assess behavior rather than hard-coded incidental values. For tasks with interactive input, provide stdin fixtures; for filesystem tasks, inspect generated files and permissions. Prefer explicit deterministic test inputs. Do not reveal full reference solutions in the learner-facing tips.