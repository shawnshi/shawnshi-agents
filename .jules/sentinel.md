## 2024-05-24 - Prompt-Based Directory Traversal
**Vulnerability:** Local agent definition files with file access tools lacked constraints against absolute paths or '../' traversals.
**Learning:** Local agents require defense-in-depth prompt constraints against path traversal when file access tools are enabled.
**Prevention:** Ensure all agents utilizing `read_file`, `search_file_content`, or `grep_search` include explicit security constraints preventing unauthorized directory traversal.