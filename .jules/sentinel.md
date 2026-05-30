## 2024-05-24 - Prompt-Based Path Traversal
**Vulnerability:** Agent definition files with file access tools lacked explicit constraints, allowing potential path traversal via prompts.
**Learning:** For LLM agents with local file tools, defense-in-depth requires explicit prompt-based security constraints since standard file system controls might not apply to the LLM's operational context.
**Prevention:** Always include a dedicated `# Security Constraints` section with strict path rules (e.g., forbidding absolute paths and `../`) immediately following the YAML frontmatter.
