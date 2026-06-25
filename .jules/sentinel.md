## 2024-06-22 - Path Traversal Prevention in Agent Definition Files
**Vulnerability:** Agents with file access tools lacked explicit prompt-based constraints against reading arbitrary absolute paths or traversing directories using '../'.
**Learning:** In prompt-based architectures, tools like `read_file` require defense-in-depth security constraints directly within the system prompt (Markdown files) to prevent unauthorized file system access, rather than solely relying on external sandbox restrictions.
**Prevention:** Always include a dedicated `# Security Constraints` section immediately following the YAML frontmatter in any agent definition file that grants file access capabilities, enforcing strict path limitations.

## 2024-06-23 - SSRF Prevention in Network-Enabled Agents
**Vulnerability:** Agents equipped with the `web_fetch` tool lacked prompt-based constraints against accessing internal network addresses, exposing the system to Server-Side Request Forgery (SSRF) vulnerabilities.
**Learning:** In prompt-based systems, granting external network access tools necessitates explicit instructions to deny access to internal subnets and cloud metadata services to prevent agents from being manipulated into probing internal infrastructure.
**Prevention:** Agents utilizing network tools like `web_fetch` must include prompt-based constraints against SSRF in their `# Security Constraints` section, explicitly blocking access to internal network addresses (e.g., 127.0.0.1) and cloud metadata services.
