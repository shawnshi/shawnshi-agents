## 2026-05-01 - Prompt-Based Path Traversal in Agent Files
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based security constraints against directory traversal, allowing agents to access absolute paths or use '../'.
**Learning:** In prompt-based repositories with AI agents, security relies on defense-in-depth through prompt constraints (e.g., `# Security Constraints`), as standard application code protections don't apply.
**Prevention:** Always ensure agent definition files that define file access tools include explicit path security constraints ("严禁通过工具访问绝对路径或包含 '../' 的路径。") immediately following the YAML frontmatter.
