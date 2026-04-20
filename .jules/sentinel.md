## 2024-04-20 - Unrestricted File Search Access in AI Agents
**Vulnerability:** AI agents defined via Markdown files have unrestricted access to file searching and reading tools (`read_file`, `search_file_content`, `grep_search`), creating a potential data exfiltration or Local File Inclusion (LFI) vector.
**Learning:** Exposing file reading capabilities to local LLM agents processing arbitrary user inputs enables path traversal vulnerabilities, especially since the repository defines global agents.
**Prevention:** Implement defense-in-depth by explicitly stripping file reading tools from agent definitions and adding a system-prompt constraint against accessing absolute or relative paths.
