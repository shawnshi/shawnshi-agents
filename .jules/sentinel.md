## 2025-02-14 - Prompt-Based Path Traversal Vulnerability
**Vulnerability:** Agents lacked constraints to prevent accessing paths with absolute paths or directory traversal via `../` when using the `read_file` tool.
**Learning:** In prompt-based pipelines relying on natural language tool calling, defense-in-depth requires explicit natural language constraints to forbid security issues like path traversal, even if standard file read access is considered a feature.
**Prevention:** Always add the explicit security constraint "严禁通过工具访问绝对路径或包含 '../' 的路径。" in all persona prompt definitions that use file reading tools.
