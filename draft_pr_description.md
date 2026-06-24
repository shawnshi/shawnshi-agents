🚨 Severity: CRITICAL
💡 Vulnerability: Agents with `web_fetch` capabilities (`book-read.md`, `youtube-research.md`) lack prompt-based constraints against Server-Side Request Forgery (SSRF), potentially allowing them to access internal network resources or cloud metadata services.
🎯 Impact: An attacker or malicious input could trick the agent into fetching internal IPs (e.g., 127.0.0.1) or cloud metadata endpoints (e.g., 169.254.169.254), leading to unauthorized internal network reconnaissance or extraction of sensitive cloud credentials.
🔧 Fix: Appended an explicit security constraint to the `# Security Constraints` section in `book-read.md` and `youtube-research.md` explicitly blocking the use of `web_fetch` for internal network addresses and cloud metadata services.
✅ Verification: Verified that the SSRF prevention constraint correctly appears in the `# Security Constraints` section immediately following the path traversal constraint in both modified markdown files.
