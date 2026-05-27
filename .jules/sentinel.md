## 2026-05-27 - Path Traversal Prevention
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit path constraints, allowing prompt-based directory traversal.
**Learning:** For agents marked as 'kind: local', file access tools are a core feature, making them vulnerable to path traversal if not constrained properly.
**Prevention:** Always include explicit security constraints preventing absolute paths and '../' in a dedicated `# Security Constraints` section immediately following the YAML frontmatter.