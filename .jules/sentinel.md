## 2024-06-22 - Path Traversal Prevention in Agent Definition Files
**Vulnerability:** Agents with file access tools lacked explicit prompt-based constraints against reading arbitrary absolute paths or traversing directories using '../'.
**Learning:** In prompt-based architectures, tools like `read_file` require defense-in-depth security constraints directly within the system prompt (Markdown files) to prevent unauthorized file system access, rather than solely relying on external sandbox restrictions.
**Prevention:** Always include a dedicated `# Security Constraints` section immediately following the YAML frontmatter in any agent definition file that grants file access capabilities, enforcing strict path limitations.
