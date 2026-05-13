## 2024-05-13 - Path Traversal in File Access Tools
**Vulnerability:** Agent definition files with file access tools lacked path constraints.
**Learning:** Prompt-based agents with file tools can be exploited for directory traversal if constraints are missing.
**Prevention:** Add explicit path traversal constraints (`严禁通过工具访问绝对路径或包含 '../' 的路径。`) to all agents utilizing file access tools in a `# Security Constraints` section.
