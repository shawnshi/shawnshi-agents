## 2024-05-24 - Path Traversal Prevention in Prompt-Based Agents
**Vulnerability:** Agents with local file access tools are vulnerable to prompt-based directory traversal (e.g., accessing absolute paths or using '../').
**Learning:** In purely prompt-based repository architectures lacking traditional code or configuration files, security constraints must be enforced via defense-in-depth prompt instructions within the agent definition files (.md).
**Prevention:** Added a dedicated '# Security Constraints' section with the standard path security constraint ('严禁通过工具访问绝对路径或包含 '../' 的路径。') immediately following the YAML frontmatter in all agent definition files utilizing file access tools.
