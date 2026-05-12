## 2026-05-12 - Missing Path Traversal Constraints in File Access Agents
**Vulnerability:** Agents with file access tools lack prompt-based constraints, making them susceptible to path traversal attacks reading absolute paths or using '../'.
**Learning:** The repository relies entirely on prompt-based constraints for security defense-in-depth since standard file tools are used deliberately.
**Prevention:** Any agent definition file utilizing file access tools must include the standard path security constraint `严禁通过工具访问绝对路径或包含 '../' 的路径。` in a dedicated `# Security Constraints` section immediately following the YAML frontmatter.
