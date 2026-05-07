## 2026-05-07 - Prompt-Based Path Traversal in Agent Definitions
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based constraints to prevent directory traversal out of the repository scope.
**Learning:** For agents marked as 'kind: local' where file access is a core feature, security against path traversal must rely on defense-in-depth prompt-based constraints since the tools themselves cannot be removed. This is a vulnerability pattern unique to this prompt-based execution environment.
**Prevention:** Always include the standard path security constraint in Chinese ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in a dedicated '# Security Constraints' section immediately following the YAML frontmatter for any agent using file access tools.
