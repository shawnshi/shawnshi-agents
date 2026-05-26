## 2024-05-26 - Prompt-Based Path Traversal
**Vulnerability:** Agent definition files utilizing file access tools lacked prompt-based constraints against absolute paths and directory traversal (e.g., '../').
**Learning:** In prompt-driven applications without traditional application code, file access tools inherently carry path traversal risks if not bounded by explicit instruction-based constraints.
**Prevention:** All agent files with file access tools must include a dedicated `# Security Constraints` section explicitly prohibiting absolute paths and '../'.
