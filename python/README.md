# General

- Pyenv

plugin [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)

In `~/  .zshrc` and `~/.zprofile`:

```
#pyenv
alias brew='env PATH="${PATH//$(pyenv root)\/shims:/}" brew'
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Use `.python-version` to set local env.

- Poetry

Deactive auto creation of venv:

    `poetry config virtualenvs.create false`