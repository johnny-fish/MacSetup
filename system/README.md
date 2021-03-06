# General

- Autocomplete:

[fig](https://github.com/withfig/autocomplete)
install it and run `fig` on terminal to finish the installation

[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) install before oh-my-zsh

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