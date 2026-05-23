## 2024-05-24 - Prevent prompt-based directory traversal
**Vulnerability:** Agent definition files utilizing file access tools lacked constraints, allowing prompt-based directory traversal.
**Learning:** In a prompt-based architecture without traditional code, security against path traversal must rely on defense-in-depth prompt constraints rather than removing essential file tools.
**Prevention:** Include the standard path security constraint ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in a dedicated `# Security Constraints` section immediately following the YAML frontmatter for any agent with file access capabilities.
