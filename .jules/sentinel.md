## 2024-05-24 - Prompt-Based Directory Traversal in Agent Definitions
**Vulnerability:** Agents with file access capabilities lack prompt-based constraints against reading arbitrary absolute or relative parent paths.
**Learning:** In a purely prompt-based AI framework, prompt-level defense-in-depth is required to prevent agents from traversing to sensitive directories using file tools.
**Prevention:** Ensure all agent definition files explicitly include the standard path security constraint in a dedicated `# Security Constraints` section.
