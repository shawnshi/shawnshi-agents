## 2024-05-24 - Missing Path Traversal Constraints in Local Agents
**Vulnerability:** Agent definition files with 'kind: local' and file access tools lacked prompt-based constraints, making them vulnerable to path traversal (e.g., accessing absolute paths or '../').
**Learning:** Prompt-based agents utilizing local file access tools require explicit defense-in-depth prompt constraints since they lack traditional sandboxing mechanisms.
**Prevention:** Always include a `# Security Constraints` section immediately following the YAML frontmatter with the constraint: "严禁通过工具访问绝对路径或包含 '../' 的路径。"
