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
"keep the local version currently installed"

## Install zsh shell & zim framework & starship & micro
```
sudo apt-get install zsh
```
```
zsh
```
```
chsh -s /usr/bin/zsh
curl -fsSL https://raw.githubusercontent.com/zimfw/install/master/install.zsh | zsh
zimfw install
```
```
curl -sS https://starship.rs/install.sh | sh
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
mkdir -p ~/.config && touch ~/.config/starship.toml
starship preset no-runtime-versions >> ~/.config/starship.toml
echo 'command_timeout = 1200\n' | cat - ~/.config/starship.toml > temp && mv temp ~/.config/starship.toml
echo '\n[aws]\ndisabled=true\n\n[gcloud]\ndisabled=true\n' >> ~/.config/starship.toml
echo '[username]\nstyle_user = "green bold"\nstyle_root = "red bold"\nformat = "[$user]($style)"\ndisabled = false\nshow_always = true\n\n[hostname]\nssh_only = false\nformat =  "[@$hostname](green bold) "\ndisabled = false' >> ~/.config/starship.toml
echo '\n[git_status]\nahead = "⇡${count}"\ndiverged = "⇕⇡${ahead_count}⇣${behind_count}"\nbehind = "⇣${count}"' >> ~/.config/starship.toml

curl https://getmic.ro | zsh
```

### Install Node LTS (v18)
```
curl -sL https://deb.nodesource.com/setup_18.x | sudo zsh -

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

### Make sure ssh has PasswordAuthentication active
```
sudo nano /etc/ssh/sshd_config
```
Locate the PasswordAuthentication attribute and set it to yes 

### Create short alias ("pn") for PNPM
```
nano ~/.zsh
```

Paste in end:
```
alias pn='pnpm'
```
then save

then source
```
source ~/.zsh
```

