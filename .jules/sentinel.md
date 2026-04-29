## 2024-05-24 - Path Traversal in Prompt-Based Agent Files
**Vulnerability:** Agent definition files (.md) with file access tools lacked explicit prompt-based constraints, making them vulnerable to path traversal (accessing absolute paths or paths with '../').
**Learning:** For agents explicitly marked as 'kind: local' where file access tools cannot be removed, defense-in-depth prompt-based constraints are critical to prevent unauthorized file access.
**Prevention:** Include the standard path security constraint ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in a dedicated `# Security Constraints` section immediately following the YAML frontmatter in all agent definition files utilizing file access tools.
