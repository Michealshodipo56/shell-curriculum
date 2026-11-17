# SH-068 — Check Service Health

**Description**

Accept a URL, make an HTTP request, and report whether it returns a successful 2xx status.

**Requirements**

Learn `curl -sS -o /dev/null -w`, timeouts, network failure handling, and the distinction between transport errors and HTTP status codes.

**Tips**

A service-health check should distinguish reachable, unhealthy, and timed-out endpoints. `curl` can request an HTTP URL and expose status codes, while `--max-time` prevents indefinite hangs. Avoid treating every HTTP response as success; define which codes count as healthy. Print a concise status and return a meaningful exit code.


**How to approach it:** Identify the required input, the expected output, and the command or Bash feature that connects them. Try a small controlled example first, then check the result against the example and the description. Keep paths and expanded variables quoted where appropriate; do not assume example paths or timestamps are fixed.

**Example**

```text
https://example.org → healthy (200)
```
