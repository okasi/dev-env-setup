
Generate & Copy SSH Key:
```
ssh-keygen -m PEM -t rsa
pbcopy < ~/.ssh/id_rsa.pub
```
Paste Here:  
https://github.com/settings/keys

<br/>

Configure user in Git CLI:
```
git config --global user.email "johndoe@example.com"
git config --global user.name "john-d"
```
