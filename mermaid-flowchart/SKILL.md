---
name: mermaid-flowchart
description: Render a Mermaid flowchart diagram from a description. The LLM converts the description to Mermaid syntax, and this skill renders it as a visual flowchart.
---

# Mermaid Flowchart Renderer

## Instructions

When the user wants to create and view a flowchart:

1. **Understand what flowchart they want** - Ask about the nodes, connections, and any styling preferences (direction, shapes, colors).

2. **Convert the description to Mermaid syntax** - Write valid Mermaid flowchart code in the format:
   ```mermaid
   flowchart TD (or LR/BT/RL)
       node1[Label] --> node2[Label]
       node2 -->|label| node3
   ```
   
   Common shapes:
   - `[Rectangle]` - rounded rectangle
   - `[Label]` - with text
   - `{Diamond}` - decision
   - `((Circle))` - circle/rounded

3. **Call the `run_js` tool** with:
   - script name: `index.html`
   - data: JSON string with field `mermaid` containing the mermaid syntax

4. Present the result to the user - the JavaScript will render the flowchart and return it as a PNG image.
