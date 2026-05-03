## 2024-05-03 - Path Traversal Prevention in Agent Definitions
**Vulnerability:** Prompt-based directory traversal using file access tools in agent definition files.
**Learning:** Agent definitions using local file tools are vulnerable to prompt injection attacks attempting to access unauthorized paths (e.g., via '../' or absolute paths).
**Prevention:** Always include a dedicated '# Security Constraints' section containing explicit path restriction directives ('严禁通过工具访问绝对路径或包含 \'../\' 的路径。') immediately following the YAML frontmatter.
