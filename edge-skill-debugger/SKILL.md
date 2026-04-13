---
name: edge-skill-debugger
description: Debug and test AI Edge Gallery skills. Import a skill URL, run its JavaScript with test data, and see results or errors.
---

# Edge Skill Debugger

## Instructions

This skill helps you debug other edge skills by loading their JavaScript and running them with test data.

When the user wants to test/debug an edge skill:

1. **Get the skill URL** - The skill's index.html must be accessible (e.g., `https://anlach.github.io/edge-skills/[skill-name]/`)

2. **Call the `run_js` tool** with:
   - script name: `index.html`
   - data: JSON string with:
     - `skillUrl`: The URL to the skill's index.html (e.g., `https://anlach.github.io/edge-skills/mermaid-flowchart/`)
     - `inputData`: The JSON data to pass to the skill's `ai_edge_gallery_get_result` function

3. **Interpret results**:
   - The debugger will load the skill's page, inject the test data, and capture any errors or returned values
   - Look for `error` field in result for problems
   - The debugger returns console.log output, return values, and any thrown errors

### Example Debug Session

To test the mermaid-flowchart skill with a simple flowchart:
```json
{
  "skillUrl": "https://anlach.github.io/edge-skills/mermaid-flowchart/",
  "inputData": {
    "mermaid": "flowchart TD\n    A[Start] --> B[End]"
  }
}
```
