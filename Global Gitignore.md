
This is awesome to generally ignore files like `.env` or `DS_Store` on your entire system without having to specify them everywhere.

```bash
touch ~/.gitignore_global

git config --global core.excludesfile ~/.gitignore_global

```