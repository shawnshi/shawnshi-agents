## 2024-05-24 - Add Path Traversal Preventions to Agents
**Vulnerability:** Prompt-based directory traversal risks in agent definition files utilizing file access tools.
**Learning:** Local agents with file access capabilities need defense-in-depth constraints directly in their prompts, as they lack standard system-level restrictions.
**Prevention:** Add a standard `# Security Constraints` section with strict path traversal rules (`严禁通过工具访问绝对路径或包含 '../' 的路径。`) immediately following the YAML frontmatter in all applicable agent definition files.
