## 2024-05-24 - Prompt-based directory traversal risk
**Vulnerability:** Agent definition files with file access capabilities lack explicit constraints, allowing potential directory traversal via prompt manipulation.
**Learning:** AI agents without strict prompt-based path limitations can be exploited to access sensitive absolute paths or relative paths (e.g., '../').
**Prevention:** Always include explicit standard path security constraints in a dedicated `# Security Constraints` section for agents with file reading/writing tools.
