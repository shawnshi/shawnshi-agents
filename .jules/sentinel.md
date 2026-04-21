## 2025-02-13 - Unrestricted File Search Access in Agent Definitions
**Vulnerability:** Agent definition files contained high-risk file access tools (read_file, search_file_content, grep_search) which could be exploited for data exfiltration or local file inclusion.
**Learning:** System-level AI agent personas were granted excessive file system permissions through their tools definitions.
**Prevention:** High-risk file tools must not be included in agent definitions. Prompt-based path traversal constraints should be added as a defense-in-depth measure.
