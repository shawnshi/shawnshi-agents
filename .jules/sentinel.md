## 2024-05-18 - Prompt-based Path Traversal Vulnerability
**Vulnerability:** Agents with local file access tools (`read_file`, etc.) lack explicit constraints against path traversal, allowing them to potentially access sensitive system files outside their intended scope via absolute paths or `../`.
**Learning:** For prompt-based agents, defense-in-depth requires explicit security directives in the agent definition, as standard sandboxing may be insufficient or misconfigured.
**Prevention:** Always inject a dedicated `# Security Constraints` section containing the path traversal prevention directive ("严禁通过工具访问绝对路径或包含 '../' 的路径。") immediately after the YAML frontmatter in any agent utilizing file tools.
