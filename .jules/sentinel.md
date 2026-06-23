## 2026-06-23 - Path Traversal Prevention
**Vulnerability:** Local file access tools in agent definitions lack path constraints, allowing potential arbitrary file read via absolute paths or directory traversal.
**Learning:** Agent definition files acting as prompt-based configurations must contain explicit path traversal preventions when file access tools are enabled, as these agents act on dynamic inputs.
**Prevention:** Always include explicit security constraints preventing absolute paths and '../' traversal directly after the YAML frontmatter in any agent prompt enabling file access capabilities.
