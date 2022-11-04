## Default macOS Terminal Theming
```
xcode-select —-install

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

```
brew install zsh zsh-completions

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

chsh -s zsh

upgrade_oh_my_zsh

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k

nano ~/.zshrc
```
Change theme to: "powerlevel10k/powerlevel10k"  

Save & Exit nano  
```
brew tap homebrew/cask-fonts

brew install --cask font-firacode-nerd-font

brew install --cask font-ubuntu-mono-nerd-font
```

Preferences > Profiles > Text > Font > UbuntuMono Nerd Font Mono > 16 pt  

Preferences > Profiles > Window > Columns > 126  

Preferences > Profiles > Window > Rows > 33  

Preferences > Profiles > Shell > When the shell exits > Close if the shell exited cleanly  

Restart Terminal  
```
p10k configure

git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

nano ~/.zshrc
```
Find "plugins=(git)"  

Append safe-paste & zsh-autosuggestions & zsh-syntax-highlighting to plugins() like this:  
```
plugins=(git safe-paste zsh-autosuggestions zsh-syntax-highlighting)
```
(Restart Terminal)  

<br/>
<br/>

## Misc macOS fixes/optimization

Allow apps from anywhere:
```
sudo spctl --master-disable
```

No delay dock:
```
defaults write com.apple.dock autohide-time-modifier -int 0;killall Dock
```

Disable mouse acceleration:
```
defaults write .GlobalPreferences com.apple.mouse.scaling -1
```

More mouse options:
```
brew cask install steermouse
```

For normal scroll w/ mouse:
```
brew cask install smoothscroll
```
<br/>
<br/>

## Tools & CLI

NodeJS LTS & pnpm & Yarn:
```
brew install pnpm
pnpm env use --global lts
brew install yarn
```

NodeJS Packages:
```
pnpm install -g prettier eslint rome@next

pnpm install -g typescript

pnpm install -g nodemon @vercel/ncc

pnpm install -g serve localtunnel now
```

Expo / React Native stuff:

Xcode:
https://download.developer.apple.com/Developer_Tools/Xcode_10.3/Xcode_10.3.xip

Android Studio:
https://developer.android.com/studio/index.html

```
brew install watchman
brew install cocoapods
brew install ios-deploy

brew tap homebrew/cask-versions
brew install --cask temurin17
export JAVA_HOME=$(/usr/libexec/java_home -v '17*')

brew cask install android-sdk
brew cask install android-platform-tools

export ANDROID_HOME=~/Library/Android/sdk/
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools

yes | sdkmanager --licenses && sdkmanager --update

adb devices
```

PHP stuff:
```
brew install composer
brew install php
```

<br/>
<br/>

## Apps
```
# To mount NTFS drives
brew install --cask Mounty

# Move and resize windows with keyboard shortcuts
brew install --cask Rectangle

# Privacy friendly web browser based on Chrome
brew install --cask Brave-browser

# Open source Firefox (web browser) fork
brew install --cask Waterfox-current

# Operating System Utilities
brew install --cask OnyX

# Disk usage utility (visualizer
brew install --cask Disk-Inventory-X

# Screenshot
brew install --cask Shottr

# Screen recorder
brew install --cask Kap

# Containerized application development
brew install --cask Docker

# IDE
brew install --cask visual-studio-code

# Android simulator
brew install --cask Genymotion

# Torrent downloader
brew install --cask qBittorrent

# Format SD cards & USB drives
brew install --cask sdFormatter

# Flash OS images to SD cards & USB drives
brew install --cask balenaEtcher

# Workspace text chat
brew install --cask Slack

# Workspace video chat
brew install --cask ZoomUs

# Community chat
brew install --cask Discord

# Private chat
brew install --cask Telegram

# Note taking
brew install --cask Notion

# Remote desktop
brew install --cask AnyDesk

# Optimize images
brew install --cask ImageOptim

# Design app
brew install --cask Figma

# Simple video editing app
brew install --cask Shotcut

# Video compression
brew install --cask HandBrake

# Handle .RAR archive files
brew install --cask The-Unarchiver

# FTP / SFTP client
brew install --cask Cyberduck

# Web Debugging Proxy
brew install --cask Charles
```
