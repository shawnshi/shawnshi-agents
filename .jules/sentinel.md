## 2024-05-24 - Path Traversal Vulnerability in Prompt Definitions
**Vulnerability:** Agent definition files utilizing file access tools (e.g., read_file) lacked explicit path security constraints, exposing a prompt-based directory traversal vulnerability.
**Learning:** In prompt-based repositories where local file tools are a core feature, defense-in-depth relies on explicit prompt constraints since standard file isolation might be insufficient.
**Prevention:** Ensure all agents with file tools include a standard security constraint preventing absolute paths or '../'.