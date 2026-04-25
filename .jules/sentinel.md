## 2026-04-25 - Prompt-Based Directory Traversal Prevention
**Vulnerability:** Local file access agents lack prompt constraints against path traversal, risking arbitrary file reads outside the intended workspace.
**Learning:** In prompt-driven architectures, defense-in-depth for file tools requires explicit textual constraints (negative constraints) because LLMs may otherwise follow user instructions to read sensitive paths like '/etc/shadow' or '../../'.
**Prevention:** Include the standard constraint '严禁通过工具访问绝对路径或包含 '../' 的路径。' in all agent definitions with file read capabilities.
