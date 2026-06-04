## 2024-06-04 - Path Traversal in Prompt-Based Agents
**Vulnerability:** Local agents with file access tools lacked explicit constraints, allowing potential path traversal via prompt injection.
**Learning:** Defense-in-depth is required for prompt-based agents; file tools shouldn't be removed, but strict path restrictions must be explicitly stated in the agent's prompt instructions.
**Prevention:** Always include a dedicated `# Security Constraints` section in agent markdown files utilizing file access tools to forbid absolute paths and `../`.
