## 2024-10-24 - Path Traversal Prevention in Prompt-Based Agents
**Vulnerability:** Prompt-based agents with local file access tools are vulnerable to directory traversal if not constrained.
**Learning:** In prompt-based repositories, defense-in-depth requires explicit security constraints in the agent's core definition file to prevent arbitrary file access.
**Prevention:** Always add a `# Security Constraints` section with path traversal constraints immediately following the YAML frontmatter in agent definitions utilizing file access tools.
