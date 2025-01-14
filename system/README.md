# General

## Terminal

- [iTerm2](https://iterm2.com/) for terminal App
- [oh-my-zsh](https://ohmyz.sh/) for zsh

## Autocomplete

- [Amazon Q (ex:fig)](https://github.com/withfig/autocomplete): Install it and launch the Amazon Q app to finish the installation.
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions): A plugin for `oh-my-zsh` that needs to be cloned into `$ZSH_CUSTOM/plugins/`.

## SSH Key

In `~/.ssh/`:

- `id_ed25519`: Default key
- `id_ed25519_personal`: Personal key

## Git

### GitConfig

In `~/.gitconfig`:
```
[user]
    name = xxx XXX
    email = xxx@xxx.com
[includeIf "gitdir:~/to_personal_path/"]
    path = ~/.gitconfig_personal
```

In `~/.gitconfig_personal`:
```
[user]
    name = xxx XXX
    email = xxx@xxx.com
[core]
    sshCommand = "ssh -i ~/.ssh/id_ed25519_personal"
```

# Mac OS System Setting

Disable the creation of .DS_Store files on external disks:
```
defaults write com.apple.desktopservices DSDontWriteNetworkStores true
```

## MacOS with M1

Use `arch -arm64` to explicitly install using the __arm__ architecture, especially in the case of:

- _pip_: `arch -arm64 pip install ...`
- _poetry_: `arch -arm64 poetry install ...`

## MacBook Air 2020 M1

- Set display resolution to 1280x800 (because the physical resolution is 2560x1600).
- Disable font smoothing (useful on low-resolution displays) with:
```
defaults -currentHost write -g AppleFontSmoothing -int 0
```
(`0: fine, 1: middle, 2: default`)
