## 2024-05-24 - Path Traversal in Prompt-Based Agents
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit constraints against directory traversal, risking unauthorized file access via prompts.
**Learning:** In prompt-based repositories without programmatic file access controls, security constraints must be enforced via explicit prompt instructions in a dedicated section.
**Prevention:** Always include a '# Security Constraints' section with strict path limitations ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in agent definitions that use file tools.
