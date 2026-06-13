## 2026-06-13 - Prevent Prompt-Based Directory Traversal
**Vulnerability:** Agent definition files with local file system tools lack path restrictions, allowing potential path traversal outside intended directories.
**Learning:** For agents utilizing file access tools, security against path traversal must rely on defense-in-depth prompt-based constraints.
**Prevention:** Always include the standard path security constraint in a dedicated `# Security Constraints` section immediately following the YAML frontmatter.
