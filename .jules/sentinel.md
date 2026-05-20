## 2024-05-20 - Prevent Path Traversal in File-Access Agents
**Vulnerability:** Agents with file-access tools (e.g., `read_file`) lack constraints preventing them from accessing arbitrary paths (e.g., `/etc/passwd` or `../`).
**Learning:** In purely prompt-based systems, security constraints must be implemented as defense-in-depth prompt instructions since traditional file system sandboxing may not be available.
**Prevention:** Ensure all agent definition files that expose file-access tools include an explicit `# Security Constraints` section forbidding absolute paths and `../`.
