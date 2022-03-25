# Mac Os System Setting

### Macbook Air 2020 M1

- set display resolution to 1280x800 (because physique resolution is 2560x1600)
- disable font smoothing (useful on low resolution display) with:  
`defaults -currentHost write -g AppleFontSmoothing -int 0`
`0: fine, 1: middle, 2: default)`