## 2024-11-26 - [Path Traversal Risk in File Tools]
**Vulnerability:** Agents using file tools lack explicit instructions preventing them from accessing absolute paths or parent directories.
**Learning:** LLM agents with read_file/search_file_content tools are susceptible to prompt injection leading to directory traversal if not constrained at the prompt level.
**Prevention:** Always include a dedicated # Security Constraints section enforcing path boundaries (e.g., 严禁通过工具访问绝对路径或包含 '../' 的路径) immediately after the YAML frontmatter.
