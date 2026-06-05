## 2024-05-24 - Missing Path Traversal Constraints
**Vulnerability:** Agent definition files with local file tools lack prompt-based constraints, allowing potential directory traversal attacks through prompts.
**Learning:** For agents utilizing file access tools (read_file, search_file_content), prompt-based constraints must be added as defense-in-depth since standard file tools are deliberately retained.
**Prevention:** Always add a `# Security Constraints` section immediately after the YAML frontmatter with explicit path restrictions in all agent definitions using file tools.
