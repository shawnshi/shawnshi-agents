## 2024-05-19 - Missing Prompt-Based Path Constraints
**Vulnerability:** Agent definition files with file access tools lacked explicit prompt-based constraints against path traversal.
**Learning:** In AI agent architectures relying on LLM-driven file access, traditional access controls must be supplemented by prompt-level defense-in-depth to prevent prompt-based directory traversal.
**Prevention:** Always include a dedicated `# Security Constraints` section with strict path traversal rules (e.g., `严禁通过工具访问绝对路径或包含 '../' 的路径。`) in any agent definition utilizing file tools.
