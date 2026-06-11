## 2024-05-24 - Prompt-Based Path Traversal Vulnerability
**Vulnerability:** Agent definition files utilizing file access tools lacked explicit prompt-based constraints against path traversal, potentially allowing access to unauthorized files.
**Learning:** For AI agents with file access, defense-in-depth requires explicit prompt-level negative constraints against path traversal, as they lack application-level input sanitization.
**Prevention:** Always include a dedicated `# Security Constraints` section with strict path traversal prohibitions in prompt architectures that expose local file read/search tools.
