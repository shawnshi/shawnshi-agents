## 2024-05-24 - Prompt-Based Path Traversal Risk
**Vulnerability:** Agent definition files with local file tools (e.g., read_file) lacked prompt-based constraints against reading arbitrary absolute paths or traversing directories using '../'.
**Learning:** Agents using LLMs can be tricked into path traversal if explicit negative constraints are missing in their system prompts, acting as a defense-in-depth measure.
**Prevention:** Always include a dedicated '# Security Constraints' section immediately after the YAML frontmatter with explicit path restrictions in Chinese for all agents utilizing file tools.
