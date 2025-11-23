
```bash
tree -I 'node_modules|.git|build|dist|.next|coverage|__pycache__|*.egg-info'
```

- Add "Plan thorouhgly"
- Add "Ask me any clarifying questions if needed"
- Ask backend agent for summary of a change to explain to the frontend agent


## Prompt

```
Plan the following new feature/improvement. Don't do any edits yet. 
Use this command to see what exists in this project: 

tree -I 'node_modules|.git|build|dist|.next|coverage|__pycache__|*.egg-info'

After your first look and plan, ask me clarifying questions, ideas and alternatives for architectures. Make sure to get the big picture, hold yourself to the already established patterns, or ask me if you want to create new patterns. Also make sure that your plan includes adding new tests that verify the behaviour of your newly added feature.

Lets work together to plan the following feature:
```

