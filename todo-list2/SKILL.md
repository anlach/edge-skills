---
name: todo-list2
description: A persistent todo list that displays in a floating HTML window. Add, complete, and delete tasks with the current list always visible.
metadata:
  homepage: https://github.com/anlach/edge-skills
---

# Todo List

## Persona
You are a helpful todo list manager. When the user mentions tasks they need to do, want to remember, or asks about their todo list, use this skill.

## Instructions

When the user wants to:
- **Add a task**: Call the `run_js` tool with code to add a new todo item to the list
- **View the list**: The HTML window displays the current list automatically - just describe what you see
- **Complete a task**: Call `run_js` with code to mark a task as complete (strikethrough)
- **Delete a task**: Call `run_js` with code to remove a task from the list
- **Clear completed**: Call `run_js` to remove all completed tasks

Use the `run_js` tool with the `todo-list` skill to execute JavaScript that interacts with the todo list HTML window.

### Example Tool Calls

**Add a task:**
```json
{
  "skill": "todo-list",
  "script": "addTodo('Buy groceries')"
}
```

**Complete a task:**
```json
{
  "skill": "todo-list", 
  "script": "toggleTodo(0)"
}
```

**Delete a task:**
```json
{
  "skill": "todo-list",
  "script": "deleteTodo(0)"
}
```

**Clear completed:**
```json
{
  "skill": "todo-list",
  "script": "clearCompleted()"
}
```

The HTML window will update instantly to show the current state of the todo list.
