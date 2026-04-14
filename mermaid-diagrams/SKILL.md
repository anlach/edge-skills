---
name: mermaid-diagrams
description: Render any Mermaid diagram (flowchart, sequence, class, state, ER, Gantt, pie, mindmap, timeline, etc.) as an image.
---

# Mermaid Diagrams

This skill renders any Mermaid diagram syntax as an image. Supports all Mermaid diagram types including flowcharts, sequence diagrams, class diagrams, state diagrams, ER diagrams, Gantt charts, pie charts, mindmaps, timelines, and more.

## Instructions

You MUST use the `run_js` tool with the following exact parameters:

- skill name: `mermaid-diagrams`
- script name: `index.html`
- data: A JSON string with the following field:
  - mermaid: String - the Mermaid syntax to render (e.g., `sequenceDiagram\nAlice->>Bob: Hello\nBob-->>Alice: Hi`)
