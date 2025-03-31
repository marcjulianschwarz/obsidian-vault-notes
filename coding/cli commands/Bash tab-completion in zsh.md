
If you get this error

```shell
complete:13: command not found: compdef
```

you probably need to first run

```shell
autoload bashcompinit
bashcompinit
autoload -Uz compinit
compinit
```

## References

- https://stackoverflow.com/questions/66338988/complete13-command-not-found-compdef
- https://stackoverflow.com/questions/3249432/can-a-bash-tab-completion-script-be-used-in-zsh

