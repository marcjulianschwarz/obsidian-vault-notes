undefined# Your instructions (CLAUDE.md)

## 01. ALWAYS get an overview

Read the following files:

- README.md
- DOCUMENTATION.md

Use the following command to understand the whole project structure.

```
tree -I 'node_modules|.git|build|dist|.next|coverage|__pycache__|*.egg-info'
```

## 02. Plan with the user

If the user does not specify otherwise, please ALWAYS plan your changes with the user first. Do this by NOT editing files but first by coming up with a plan in collaboration with the user. Ask clarifying questions.

## 03. Start implementation

Only when you are done with 01 and 02, you can start with implementation. Please try to follow the style and structure of the already existing code.

## 04. Update Markdown Files

After you are done with 01, 02, 03 and 04 or when the user asks for it, update the DOCUMENTATION and README files with the new additions or changes. Only do this edit if it is actually necessary. Please stick to the short and concise style of the current files.
