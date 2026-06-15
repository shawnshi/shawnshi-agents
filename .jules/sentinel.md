## 2024-06-15 - Prompt-based Directory Traversal Prevention
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit security constraints to prevent path traversal via prompt injection.
**Learning:** In prompt-based systems without traditional application code, defense-in-depth security requires explicitly instructing agents in their prompts (Markdown files) to reject absolute paths or paths containing '../'.
**Prevention:** Always include a dedicated `# Security Constraints` section with strict path traversal prohibitions immediately following the YAML frontmatter in any agent definition utilizing file tools.
