
- Add "Plan thorouhgly"
- Add "Ask me any clarifying questions if needed"
- Ask backend agent for summary of a change to explain to the frontend agent
- Do NOT use auto compaction, instead often reset the context in between new features with /reset or by quitting and running claude code again


## General CLAUD.md structure 

```md
# CLAUDE.md

Read:
- README.md
- DOCUMENTATION.md
- services/frontend/README.md
- services/backend/README.md
  
Use
tree -fi -I 'node_modules|.git|build|dist|.next|coverage|__pycache__|*.egg-info|data|htmlcov'
to get all paths. Never use the Explore tool, you can just read the paths from the tree command.
```


## Logging

- https://blog.fsck.com/2025/12/02/helping-agents-debug-webapps/
- setup an endpoint to send all frontend logs to (at least in development)
- let claude code tail the backend logs



