Start PowerShell as Admin

## Package manager & essentials
https://chocolatey.org/
```
powershell -noprofile -command "Install-Module PSReadLine -Force -SkipPublisherCheck"

Set-ExecutionPolicy Bypass -Scope Process

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install git -y
choco install git-lfs -y

choco install nerd-fonts-firacode -y
choco install nerd-fonts-ubuntumono -y

choco install vscode -y

choco install peazip -y
```

Close PowerShell


## Terminal & shell


Now open GIT Bash as Admin

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

## Alacritty setup
```
mkdir ~/AppData/Roaming/alacritty

touch ~/AppData/Roaming/alacritty/alacritty.yml

nano ~/AppData/Roaming/alacritty/alacritty.yml
```
Paste & save this:
```
shell:
  program: C:\Program Files\Git\bin\bash.exe
  args:
  - --login

window:
    dimensions:
        columns: 128
        lines: 36

font:
    size: 14
    normal:
        family: UbuntuMono Nerd Font Mono

selection:
    save_to_clipboard: true

mouse:
    hints:
        launcher:
            program: open
        modifiers: Command

alt_send_esc: false

key_bindings:
    - { key: Left,     mods: Alt,     chars: "\x1bb"                       }
    - { key: Right,    mods: Alt,     chars: "\x1bf"                       }
    - { key: Left,     mods: Command, chars: "\x1bOH",   mode: AppCursor   }
    - { key: Right,    mods: Command, chars: "\x1bOF",   mode: AppCursor   }
    - { key: Back,     mods: Command, chars: "\x15"                        }
    - { key: Back,     mods: Alt,     chars: "\x1b\x7f"                    }
    - { key: V, mods: Control, action: Paste }
    - { key: C, mods: Control, action: Copy }
    - { key: C, mods: Control|Shift, chars: "\x03" }

colors:
    primary:
        background: '#0d1117'
        foreground: '#ffffff'
    cursor:
        text: '#F81CE5'
        cursor: '#ffffff'
    normal:
        black:   '#000000'
        red:     '#fe0100'
        green:   '#33ff00'
        yellow:  '#feff00'
        blue:    '#0066ff'
        magenta: '#cc00ff'
        cyan:    '#00ffff'
        white:   '#d0d0d0'
    bright:
        black:   '#808080'
        red:     '#fe0100'
        green:   '#33ff00'
        yellow:  '#feff00'
        blue:    '#0066ff'
        magenta: '#cc00ff'
        cyan:    '#00ffff'
        white:   '#FFFFFF'

```

Start Alacritty

## Programming languages
```
choco install python -y
choco install temurin17 -y
choco install nodejs-lts -y
choco install pnpm -y
pnpm setup
pnpm env use --global lts
```

## Some aliases & tools
```
echo 'alias nano="micro"' >> ~/.zshrc
git config --global core.editor "micro"

choco install lsd -y
echo 'alias ls="lsd"' >> ~/.zshrc
echo 'alias l="ls -l"' >> ~/.zshrc
echo 'alias la="ls -a"' >> ~/.zshrc
echo 'alias lla="ls -la"' >> ~/.zshrc
echo 'alias lt="ls --tree"' >> ~/.zshrc

choco install bat -y
echo 'alias cat="bat"' >> ~/.zshrc

echo 'alias pbcopy="xclip -selection clipboard"' >> ~/.zshrc
echo 'alias pbpaste='xclip -selection clipboard -o'' >> ~/.zshrc

source ~/.zshrc
```

<br/>
