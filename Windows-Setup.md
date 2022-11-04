# Use PowerShell only


# Powershell stuff
```
Install-Module -Name PowerShellGet -Force
Install-Module -Name posh-git -AllowPrerelease -Force
powershell -noprofile -command "Install-Module PSReadLine -Force -SkipPublisherCheck"
```

# Enable WSL
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Install:
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

Restart
```
wsl --set-default-version 2

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install curl wget git build-essential libssl-dev
```

# Package manager & essentials
https://chocolatey.org/
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco install wsl-ubuntu-2004

choco install fluent-terminal

choco install git
choco install git-lfs

choco install nodejs-lts
choco install python
choco install temurin17

choco install firacodenf

choco install vscode

sudo apt-get update
sudo apt-get upgrade

sudo apt-get install xclip xsel
sudo apt-get install wget ca-certificates
```

# ZSH
```

sudo apt-get install zsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k

nano ~/.zshrc
```

Paste the next line ZSH_THEME="powerlevel9k/powerlevel9k" instead of ZSH_THEME="robbyrussell"

```
nano ~/.bashrc
```
Add `bash -c zsh` to top of file


# NodeJS
https://github.com/creationix/nvm#install-script
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash

nano ~/.zshrc
```
Paste
```
export NVM_DIR=~/.nvm
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
```
Save
```
source ~/.zshrc
nvm install --lts
nvm use --lts
```

# pbcopy alias
```
nano ~/.zshrc
```
Paste
```
alias pbcopy='xclip -selection clipboard'
alias pbpaste='xclip -selection clipboard -o'
```
Save
```
source ~/.zshrc
```

https://github.com/dracula/powershell

<br/>


