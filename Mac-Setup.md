## Default macOS Terminal Theming
```
xcode-select —-install

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

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

brew cask install font-firacode-nerd-font

brew cask install font-firacode-nerd-font-mono

brew cask install font-hack-nerd-font

brew cask install font-sourcecodepro-nerd-font-mono

brew cask install font-ubuntumono-nerd-font

brew cask install font-meslolg-nerd-font
```
Restart terminal  

Preferences > Profiles > Text > Font > Meslo LG S Nerd Font Mono > 14 pt  

Preferences > Profiles > Window > Columns > 100  

Preferences > Profiles > Shell > When the shell exits > Close if the shell exited cleanly  

Restart Terminal  
```
p10k configure

git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

nano ~/.zshrc
```
Find "plugins=(git)"  

Append zsh-autosuggestions & zsh-syntax-highlighting to plugins() like this:  
```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
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

App to mount NTFS drives:
```
brew cask install mounty
```
<br/>
<br/>

## Tools & CLI

NodeJS LTS:
```
brew install node@12
brew link --overwrite node@12 --force
brew install yarn
```

NodeJS Packages:
```
npm install -g nodemon
npm install -g serve
npm install -g prettier
npm install -g eslint
npm install -g now
npm install -g typescript
npm install -g apollo
npm install -g expo-cli
npm install -g gatsby-cli
```

Expo stuff:
```
brew install watchman
brew cask install android-platform-tools
adb devices
```

PHP stuff:
```
brew install composer
brew install php
```

Java:
```
brew tap AdoptOpenJDK/openjdk
brew cask install adoptopenjdk11
```

<br/>
<br/>

## Apps
```
brew cask install Keka

brew cask install Spectacle

brew cask install Brave-browser

brew cask install Waterfox-current

brew cask install OnyX

brew cask install Disk-inventory-x

brew cask install Joplin

brew cask install Kap

brew cask install Docker

brew cask install Visual-studio-code

brew cask install Insomnia

brew cask install Genymotion

brew cask install qBittorrent

brew cask install sdFormatter

brew cask install balenaEtcher

brew cask install Slack

brew cask install Telegram

brew cask install TeamViewer

brew cask install ImageOptim

brew cask install Figma

brew cask install Shotcut

brew cask install HandBrake

brew cask install Postgres

Lightshot Screenshot

CleanMyMac X

Postico

Transmit
```

If you need Adobe Illustrator & After Effects use the 2015.3 version, it's the most compatible and stable.
