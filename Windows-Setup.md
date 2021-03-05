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

wsl --set-default-version 2

```

Package manager & essentials
https://chocolatey.org/
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco install wsl-ubuntu-2004

choco install fluent-terminal

choco install git
choco install git-lfs

choco install nodejs-lts
choco install python

choco install firacodenf

choco install vscodium
```



https://github.com/dracula/powershell

<br/>


