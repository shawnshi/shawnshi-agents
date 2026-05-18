## 2024-05-24 - Fix prompt-based directory traversal
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based security constraints to prevent directory traversal.
**Learning:** For local agents where file tools cannot be removed, defense-in-depth prompt-based constraints are necessary to prevent directory traversal.
**Prevention:** Always include `# Security Constraints` immediately following the YAML frontmatter with rules against absolute paths and '../' for agents with file tools.
