# Tools
- visual studio code https://code.visualstudio.com/download latest
- intellij / webstorm eap https://www.jetbrains.com/resources/eap latest
- sourcetree https://www.sourcetreeapp.com/download-archives v2.7.6
- homebrew https://brew.sh latest
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- nvm latest
```
brew install nvm

add to ~/.profile

export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/usr/local/opt/nvm/etc/bash_completion" ] && . "/usr/local/opt/nvm/etc/bash_completion"  # This loads nvm bash_completion
```
- nodejs
```
nvm install node
```
- yarn
```
brew install yarn
``` 

# Environment
## ssh
```
ssh-add ~/.ssh/some-ssh-key
```