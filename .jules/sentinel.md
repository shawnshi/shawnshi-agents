## 2024-05-18 - Missing path traversal constraint in markdown agents
**Vulnerability:** Many agents utilizing file access tools (e.g. read_file, search_file_content) are missing constraints against path traversal in their prompt instructions.
**Learning:** For prompt-based agents that process user instructions and can access files, missing explicit constraints against absolute paths or parent directories (`../`) can lead to arbitrary file reads by malicious prompt injection.
**Prevention:** Always include the standard path security constraint `# Security Constraints\n严禁通过工具访问绝对路径或包含 '../' 的路径。` immediately after the YAML frontmatter in any agent configuration file.
