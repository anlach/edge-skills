---
name: mermaid-flowchart
description: Render a Mermaid flowchart diagram from a description. The LLM converts the description to Mermaid syntax, and this skill renders it as SVG.
---

# Mermaid Flowchart Renderer

## Instructions

When the user wants to create and view a flowchart:

1. **Understand what flowchart they want** - Ask about the nodes, connections, and layout.

2. **Convert the description to Mermaid syntax** - Write valid Mermaid code:
   ```mermaid
   flowchart TD
       node1[Label] --> node2[Label]
   ```
   
   Common shapes:
   - `[Rectangle]` - rounded rectangle
   - `{Diamond}` - decision
   - `((Circle))` - circle

3. **Call the `run_js` tool** with:
   - script name: `index.html`
   - data: `{"mermaid": "flowchart TD\\n    A[Start] --> B[End]"}`

4. The skill returns SVG which will be displayed to the user.
