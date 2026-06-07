## 2024-05-15 - Missing Path Traversal Constraints in Local Agents
**Vulnerability:** Agent definition files utilizing local file access tools (read_file, search_file_content) lacked explicit constraints against reading absolute paths or traversing directories using '../', potentially leading to prompt-based directory traversal.
**Learning:** For agents explicitly marked as 'kind: local', file access tools are core features and must be secured via defense-in-depth prompt-based constraints rather than tool removal.
**Prevention:** Always add a `# Security Constraints` section immediately after the YAML frontmatter containing standard path security constraints ("严禁通过工具访问绝对路径或包含 '../' 的路径。") for agents with file access tools.
