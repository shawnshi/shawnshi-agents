## 2024-05-24 - Missing Security Constraints in Agent Markdown Files
**Vulnerability:** Agent definition files utilizing file access tools lacked path security constraints, allowing potential prompt-based directory traversal.
**Learning:** In a prompt-based repository with no traditional application code, prompt-based constraints act as defense-in-depth measures against directory traversal when file tools are deliberately retained.
**Prevention:** Always include standard path security constraints ("严禁通过工具访问绝对路径或包含 '../' 的路径。") in agent definition files that use file access tools.
