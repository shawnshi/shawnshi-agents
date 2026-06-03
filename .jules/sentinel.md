## 2024-05-24 - [Path Traversal Prevention in Agent Definitions]
**Vulnerability:** Agent definition files utilizing file access tools (e.g., read_file) lack explicit constraints against prompt-based directory traversal.
**Learning:** For agents marked as 'local' where file access tools are core features, path traversal protection must rely on defense-in-depth prompt-based constraints rather than removing the tools.
**Prevention:** Include a dedicated `# Security Constraints` section immediately following the YAML frontmatter containing the instruction "严禁通过工具访问绝对路径或包含 '../' 的路径。" in all affected agent files.
