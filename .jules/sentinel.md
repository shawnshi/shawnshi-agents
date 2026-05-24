## 2026-05-24 - Path Traversal Prevention in File Tools
**Vulnerability:** Agent definition files (.md) with file access tools (read_file, search_file_content, etc.) lacked constraints against directory traversal, allowing potential read access outside the intended scope via prompt injection.
**Learning:** Even explicitly scoped agents ('kind: local') require defense-in-depth prompt-based constraints when file access tools are enabled, as the tools themselves might not enforce absolute path boundaries.
**Prevention:** Ensure any agent definition file utilizing file access tools includes the standard path security constraint ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in a dedicated `# Security Constraints` section immediately following the YAML frontmatter.
