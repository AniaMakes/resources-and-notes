# A rough guide to setting up a Mac for dev work

## Basics
- git
- npm
- code editor of choice (and any extensions you like)

## Dev tools (as needed)
- nvm
- git GUI manager (GitHub Desktop)
- vault
- insomnia
- postman
- charles (call interceptor / investigator)

### Git autocompletion in bash
`curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash`

then add the following to `~/.bash_profile`
```
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```
from [StackExchange](https://apple.stackexchange.com/questions/55875/git-auto-complete-for-branches-at-the-command-line)

### Chown some files to avoid needing sudo in the future for global npm installs
`sudo chown $USER /usr/local/*`

## Quality of life
- window snapping software (Magnet)
- Spotify
- VLC
