# General

- Terminal

[iTerm2](https://iterm2.com/) for terminal App

[oh-my-zsh](https://ohmyz.sh/) for zsh

- Autocomplete:

[fig](https://github.com/withfig/autocomplete)
install it and run `fig` on terminal to finish the installation

[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) is a plugin of `oh-my-zsh` need to be clone in `$ZSH_CUSTOM/plugins/`

- SSH Key

In `~/.ssh/`:

`id_ed25519` default key

`id_ed25519_personal` personal key

- Git

GitConfig

`~/.gitconfig`
```
[user]
    name = xxx XXX
    email = xxx@xxx.com
[includeIf "gitdir:~/to_personal_path/"]
    path = ~/.gitconfig_personal
```
`~/.gitconfig_personal`
```
[user]
    name = xxx XXX
    email = xxx@xxx.com
[code]
    sshCommand = "ssh -i ~/.ssh/id_ed25519_personal"
```

# Mac Os System Setting

Disable to create .DS_Store file on extern disk:

`defaults write com.apple.desktopservices DSDontWriteNetworkStores true`

### MacOS with M1

- `arch -arm64` tell explicitly to install using __arm__ architecture  

especially in the case of:

_pip_: `arch -arm64 pip install ...`  
_peotry_: `arch -arm64 peotry install ...`

### Macbook Air 2020 M1

- set display resolution to 1280x800 (because physique resolution is 2560x1600)
- disable font smoothing (useful on low resolution display) with:  
`defaults -currentHost write -g AppleFontSmoothing -int 0` `0: fine, 1: middle, 2: default)`