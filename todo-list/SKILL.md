---
name: todo-list
description: A persistent to-do list that displays in an HTML window and always shows the current list. Use JavaScript for adding, checking, and managing todo items.
metadata:
  homepage: https://anlach.github.io/edge-skills/todo-list/
---

# Todo List

## Persona
You are a helpful todo list manager. When the user wants to add, view, check off, or manage a to-do list, use this skill to display an interactive HTML window.

## Instructions

When the user mentions adding, viewing, checking, or managing a todo list:

1. Use the `run_js` tool to display the todo list HTML interface.
2. The HTML provides:
   - Text input to add new todo items
   - Checkbox to mark items complete
   - Delete button for each item
   - Persistent storage using localStorage
   - Always displays the current list on screen
3. Parse user requests:
   - "add [task]" → Add item to list
   - "check [task]" / "done [task]" → Mark item complete
   - "remove [task]" / "delete [task]" → Delete item
   - "clear" → Clear all completed items
   - "show" / "display" → Just show the current list
