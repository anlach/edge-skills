---
name: mermaid-flowchart
description: Render a Mermaid flowchart as an image.
---

# Mermaid Flowchart

This skill renders Mermaid flowchart syntax as an image.

## Instructions

You MUST use the `run_js` tool with the following exact parameters:

- skill name: `mermaid-flowchart`
- script name: `index.html`
- data: A JSON string with the following field:
  - mermaid: String - the Mermaid flowchart syntax to render (e.g., `flowchart TD\nA[Start] --> B[End]`)
