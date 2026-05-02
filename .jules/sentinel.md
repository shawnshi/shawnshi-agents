## 2024-05-18 - Prevent Directory Traversal via Prompt Constraints
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based security constraints, creating a risk of directory traversal attacks.
**Learning:** For prompt-based systems lacking standard configurations, defense-in-depth requires explicit constraints within the agent definition to prevent unauthorized file access.
**Prevention:** Include the standard path security constraint ('严禁通过工具访问绝对路径或包含 '../' 的路径。') in a dedicated `# Security Constraints` section immediately following the YAML frontmatter for all agent files using file tools.
