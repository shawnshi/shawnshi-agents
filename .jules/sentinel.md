## 2024-05-29 - Missing Path Traversal Constraints in Prompts
**Vulnerability:** Agent definition files with file access tools lack explicit path security constraints, allowing potential prompt-based directory traversal.
**Learning:** Explicit prompt constraints acting as defense-in-depth are necessary to prevent traversal when file access tools cannot be removed.
**Prevention:** Always add a dedicated `# Security Constraints` section immediately after the YAML frontmatter containing the constraint against accessing absolute paths or paths with '../'.
