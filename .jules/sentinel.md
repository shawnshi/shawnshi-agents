## 2024-05-26 - Prompt-based Path Traversal Risk
**Vulnerability:** Agent files with file access tools lacked constraints against reading absolute or parent directory paths, enabling potential path traversal via prompt injection.
**Learning:** Prompt-based repositories must rely on defense-in-depth prompt constraints when file tools are deliberately retained.
**Prevention:** Always add a `# Security Constraints` section immediately after the YAML frontmatter containing the path constraint when creating or modifying agents with local file tools.
