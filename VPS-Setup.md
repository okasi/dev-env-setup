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

### Install Node LTS (v16)
```
curl -sL https://deb.nodesource.com/setup_16.x | sudo bash -

sudo apt-get install -y nodejs && sudo apt-get update
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
git config --global user.email "okasi@pm.me"
git config --global user.name "okasi"
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
