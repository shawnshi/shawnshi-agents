## 2024-05-24 - Path Traversal Prevention in Prompt-Based Agents
**Vulnerability:** Prompt-based agents with local file access tools are susceptible to directory traversal attacks if path inputs are not constrained.
**Learning:** In purely prompt-based agent architectures, security relies heavily on defense-in-depth prompt constraints since traditional application-level input sanitization is absent.
**Prevention:** Add explicit path security constraints ("严禁通过工具访问绝对路径或包含 '../' 的路径。") immediately following the YAML frontmatter in all agent definition files that utilize file access tools.
