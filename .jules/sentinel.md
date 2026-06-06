## 2024-05-24 - Missing Path Traversal Security Constraints
**Vulnerability:** Prompt-based agent definition files using local file tools lack path traversal constraints.
**Learning:** In prompt-based setups, agents with file access must be explicitly restricted from accessing absolute paths or moving up directories to prevent unauthorized system access.
**Prevention:** Always add a `# Security Constraints` section with strict path rules immediately following the YAML frontmatter for agents using file tools.