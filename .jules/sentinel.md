## 2024-05-24 - Missing Path Traversal Constraints in Agent Definitions
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based security constraints against directory traversal.
**Learning:** In prompt-based execution environments, omitting explicit file access boundaries allows agents to interpret implicit permission to access restricted paths, necessitating a defense-in-depth approach.
**Prevention:** Always place a dedicated `# Security Constraints` section immediately following the YAML frontmatter with the standard path traversal constraint in Chinese when file tools are present.
