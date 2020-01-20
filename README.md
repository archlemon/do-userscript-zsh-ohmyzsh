# do-userscript-zsh-ohmyzsh

```
#!/bin/bash

apt-get -y update
apt-get -y upgrade
apt-get -y install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i "" 's/^plugin(/plugin(docker docker-compose dotenv git ssh-agent zsh-autosugestions' ~/.zshrc
chsh -s /usr/bin/zsh root
```
