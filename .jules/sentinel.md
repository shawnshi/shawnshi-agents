## 2024-04-23 - Prevent Path Traversal in Local Agents
**Vulnerability:** Local prompt-based agents have unrestricted file tools (`read_file`, `search_file_content`, etc.), allowing arbitrary file reads on the system via path traversal (e.g. `../` or `/etc/passwd`).
**Learning:** For prompt-based agents that require file access, standard software security tools (like chroot or removing the tool) aren't applicable. Prompt-based constraints must be used as defense-in-depth to enforce sandbox boundaries.
**Prevention:** Always add the standard prompt constraint "严禁通过工具访问绝对路径或包含 '../' 的路径。" to any agent with `kind: local` and file access tools.
