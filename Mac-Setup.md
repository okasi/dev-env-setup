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

brew cask install font-firacode-nerd-font

brew cask install font-hack-nerd-font

brew cask install font-ubuntumono-nerd-font

brew cask install font-meslolg-nerd-font
```

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

NodeJS LTS:
```
brew install node@12
brew link --overwrite node@12 --force
ln -s /usr/local/opt/node@12 /usr/local/opt/node
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

Expo / React Native stuff:

Xcode:
https://download.developer.apple.com/Developer_Tools/Xcode_10.3/Xcode_10.3.xip

Android Studio:
https://developer.android.com/studio/index.html

```
brew install watchman
brew install cocoapods
brew install ios-deploy

brew cask install adoptopenjdk/openjdk/adoptopenjdk8
export JAVA_HOME=$(/usr/libexec/java_home -v 1.8) 

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
brew cask install Mounty

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
