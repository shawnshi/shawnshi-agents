## 2024-06-22 - Path Traversal Prevention in Agent Definition Files
**Vulnerability:** Agents with file access tools lacked explicit prompt-based constraints against reading arbitrary absolute paths or traversing directories using '../'.
**Learning:** In prompt-based architectures, tools like `read_file` require defense-in-depth security constraints directly within the system prompt (Markdown files) to prevent unauthorized file system access, rather than solely relying on external sandbox restrictions.
**Prevention:** Always include a dedicated `# Security Constraints` section immediately following the YAML frontmatter in any agent definition file that grants file access capabilities, enforcing strict path limitations.

## 2024-10-24 - SSRF Prevention in Agents with Web Fetch
**Vulnerability:** Agents with `web_fetch` capabilities lack prompt-based constraints against Server-Side Request Forgery (SSRF), potentially allowing them to access internal network resources or cloud metadata services.
**Learning:** In prompt-based systems, tools that fetch URLs must be constrained within the system prompt to explicitly block access to local/private IP ranges and metadata endpoints.
**Prevention:** Always include SSRF prevention constraints (blocking 127.0.0.1, localhost, 169.254.169.254, etc.) in the `# Security Constraints` section for any agent utilizing `web_fetch` or similar network tools.
