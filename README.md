# do-userscript-zsh-ohmyzsh

```
#!/bin/bash

RUNZSH=no

apt-get -y update
apt-get -y install zsh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
sed -i 's/^plugins=(git)/plugins=(docker docker-compose dotenv git ssh-agent zsh-autosuggestions)/' ~/.zshrc
sed -i 's/^ZSH_THEME=\"robbyrussell\"/ZSH_THEME=\"agnoster\"/' ~/.zshrc
chsh -s $(which zsh) root
```
