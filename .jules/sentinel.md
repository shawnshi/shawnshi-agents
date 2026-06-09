## 2024-05-26 - Prompt-Based Path Traversal Vulnerability
**Vulnerability:** Agent definition files utilizing file access tools (like read_file) lack explicit path traversal constraints, making them vulnerable to prompt injection attacks targeting absolute paths or `../`.
**Learning:** In prompt-based architectures without traditional application code, file access tools must be secured via defense-in-depth prompt constraints within the agent definition itself.
**Prevention:** Always include a dedicated `# Security Constraints` section immediately following the YAML frontmatter specifying path access limitations.
