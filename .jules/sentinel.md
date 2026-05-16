## 2026-05-16 - Path Traversal Vulnerability in Local Agents
**Vulnerability:** Agent definition files with file access tools lack prompt-based path traversal constraints, allowing access to arbitrary directories.
**Learning:** Local agents require prompt-based defense-in-depth constraints to prevent accessing paths outside their intended scope using relative or absolute paths.
**Prevention:** Add a dedicated `# Security Constraints` section with the exact text "严禁通过工具访问绝对路径或包含 '../' 的路径。" immediately after the YAML frontmatter in any agent definition file utilizing file access tools.