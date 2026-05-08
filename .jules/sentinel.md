## 2024-05-08 - Agent Prompt Path Traversal Prevention
**Vulnerability:** Agents with local file access tools (`read_file`, etc.) lacked constraints against prompt-based directory traversal (accessing absolute paths or paths with `../`).
**Learning:** In prompt-based LLM applications without standard code security constraints, defense-in-depth relies on explicitly injecting path security constraints directly into the agent persona definitions.
**Prevention:** Always enforce the standard path security constraint ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in a dedicated `# Security Constraints` section directly below the YAML frontmatter for any agent utilizing file access tools.
