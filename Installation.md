# Setup Node.JS on Ubuntu 16.04
```shell
sudo apt-get update -y
sudo apt-get install -y build-essential libssl-dev libreadline-dev zlib1g-dev
```

## Install NVM
```shell
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.39.0/install.sh | bash
```

The script clones the nvm repository to \~/.nvm and adds the source line to your profile  
(~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc).
```shell
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```
```shell
# Example
echo $'export NVM_DIR="$HOME/.nvm"\n[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"\n[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"' >> ~/.bash_profile
```

## Install node.js with NVM
```shell
# Install LTS
nvm install --lts
nvm alias default lts/*
```
