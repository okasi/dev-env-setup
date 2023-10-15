Start PowerShell as Admin:
- Windows+R to open run window
- Type "Powershell"
- Ctrl+Shift+Enter to open with admin privileges 


## Package manager Chocolatey
https://chocolatey.org/
```
powershell -noprofile -command "Install-Module PSReadLine -Force -SkipPublisherCheck"

Set-ExecutionPolicy Bypass -Scope Process

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Optional programs
```
choco install opera -y
choco install qbittorrent -y
choco install peazip.install -y
choco install discord -y
choco install steam -y
choco install vlc -y
choco install irfanview -y
choco install lightshot -y
choco install vscode-insiders -y
choco install windirstat -y
choco install open-shell -y
choco install notepadplusplus.install -y
```


Dev essentials
```
choco install git -y
choco install git-lfs -y

choco install nerd-fonts-firacode -y
choco install nerd-fonts-ubuntumono -y

choco install vscode -y
```

Close PowerShell


## Terminal & shell

Now open Git Bash as Admin

Setup autocomplete files
```
mkdir ~/bash_completion.d   
curl -o ~/bash_completion.d/git https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
echo "source ~/bash_completion.d/git" >> ~/.bashrc
```

Install oh my bash:
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

Save

```
choco install lsd -y
choco install bat -y
choco install micro -y

```


## Some aliases & tools
```
echo 'alias nano="micro"' >> ~/.bashrc
git config --global core.editor "micro"

echo 'alias ls="lsd"' >> ~/.bashrc
echo 'alias l="ls -l"' >> ~/.bashrc
echo 'alias la="ls -a"' >> ~/.bashrc
echo 'alias lla="ls -la"' >> ~/.bashrc
echo 'alias lt="ls --tree"' >> ~/.bashrc

echo 'alias cat="bat"' >> ~/.bashrc

echo 'alias pbcopy="xclip -selection clipboard"' >> ~/.bashrc
echo 'alias pbpaste="xclip -selection clipboard -o"' >> ~/.bashrc

source ~/.bashrc
```


## Git bash theme
- Text
  - UbuntuMono Nerd Font Mono, 11pt
- Window
  - Columns: 128
  - Rows: 36


## Programming languages
```
choco install python -y
choco install nodejs-lts -y
```
