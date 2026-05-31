## 2024-05-24 - Path Traversal in Agent Definitions
**Vulnerability:** Agents with file access tools lacked path traversal constraints, allowing prompt-based directory traversal.
**Learning:** Prompt-based directory traversal must be actively prevented in agent definitions when using file tools.
**Prevention:** Added explicit defense-in-depth '# Security Constraints' to all agent definition files equipped with file tools to strictly prohibit absolute and '../' paths.
