### If you need to rent a good cheap VPS
https://cloud.hosthatch.com/a/2831

### To connect w/ password in one line from local machine (Mac)
```
brew tap esolitos/ipa
brew install sshpass

sshpass -p <PASS> ssh <USER>@<IP/DOMAIN> -X
```

### Stand in root
```
cd ~
```

### Update stuff
```
sudo apt update && sudo apt upgrade -y 
```

### Install essentials
```
sudo apt install curl wget xclip && sudo apt-get install gcc g++ make
```

## Install fish shell & starship
```
sudo apt-get install fish
fish
chsh -s /usr/bin/fish
mkdir -p ~/.config/fish
echo "set -g -x fish_greeting ''" >> ~/.config/fish/config.fish

curl -sS https://starship.rs/install.sh | sh
echo "starship init fish | source" >> ~/.config/fish/config.fish
mkdir -p ~/.config && touch ~/.config/starship.toml
starship preset bracketed-segments > ~/.config/starship.toml
```

### Install Node LTS (v18)
```
curl -sL https://deb.nodesource.com/setup_18.x | sudo bash -

sudo apt-get install -y nodejs && sudo apt-get update
```

### Install yarn
```
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```

### Install PNPM
```
curl -fsSL https://get.pnpm.io/install.sh | sh -
```

### Install pm2
```
pnpm i -g pm2
```

### Generate SSH key
```
ssh-keygen -m PEM -t rsa
```

### Paste in Github
```
cat ~/.ssh/id_rsa.pub
```

### Config git
```
git config --global user.email "<GITHUB EMAIL>"
git config --global user.name "<GITHUB USERNAME>"
```

### Create short alias ("pn") for PNPM
```
nano ~/.bashrc
```

Paste in end:
```
alias pn='pnpm'
```
then save

then source
```
source ~/.bashrc
```

### Install cloudpanel
```
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo bash
```
