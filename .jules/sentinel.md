## 2026-05-17 - Missing Path Traversal Constraints in Agent Markdown Files
**Vulnerability:** Agent definition files with file access tools lacked explicit constraints against accessing arbitrary paths (e.g. absolute paths or paths with '../').
**Learning:** In a pure prompt-based repository, file tools are deliberate features. Path traversal prevention must rely on defense-in-depth prompt-based constraints inside the agent markdown.
**Prevention:** Ensure every agent definition file with file access tools includes the standard constraint '严禁通过工具访问绝对路径或包含 '../' 的路径。' in a '# Security Constraints' section immediately following the YAML frontmatter.
