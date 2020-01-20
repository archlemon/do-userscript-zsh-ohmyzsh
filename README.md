# do-userscript-zsh-ohmyzsh

```
#!/bin/bash

RUNZSH=no

apt-get -y update
apt-get -y install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i 's/^plugins=(git)/plugins=(docker docker-compose dotenv git ssh-agent zsh-autosuggestions)/' ~/.zshrc
sed -i 's/^ZSH_THEME=\"robbyrussell\"/ZSH_THEME=\"agnoster\"/' ~/.zshrc
chsh -s /usr/bin/zsh root
```
