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
  - mermaid: String - the Mermaid syntax to render (e.g., `{"mermaid": "sequenceDiagram\\nAlice->>Bob: Hello\\nBob-->>Alice: Hi"}`)

## Important Syntax Rules

### Gantt Charts (most common source of errors)

Mermaid's Gantt parser treats commas as field separators. Task lines use this format:

```
Task Title :taskID, startDate, duration
```

**DO NOT** put extra text after the colon and before the task ID with commas in it. This will fail:

```
❌ Task A: Requirements Gathering, a1, 2024-01-01, 7d
```

Mermaid reads "Task A: Requirements Gathering" as the title, then expects a task ID but finds `, a1` which it can't parse. Instead use one of these correct formats:

```
✅ Requirements Gathering          :a1, 2024-01-01, 7d
✅ Task A                          :a1, 2024-01-01, 7d
```

The task title is everything before the colon. After the colon comes the task ID (optional), then comma-separated fields.

### Pie Charts

Pie chart labels with special characters or quotes must use proper escaping:

```
pie title Pet Ownership
    "Dogs" : 386
    "Cats" : 85
```
