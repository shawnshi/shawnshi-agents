## 2024-06-01 - Add Path Traversal Prevention
**Vulnerability:** Agent definition files utilizing file access tools lacked path traversal constraints, potentially allowing prompts to access arbitrary files.
**Learning:** For agents explicitly marked as 'kind: local' or using file access tools, the tools are a core feature and must not be removed. Security against path traversal must rely on defense-in-depth prompt-based constraints.
**Prevention:** Always add a `# Security Constraints` section with the standard path security constraint `严禁通过工具访问绝对路径或包含 '../' 的路径。` immediately following the YAML frontmatter in agent definition files that use file tools.
