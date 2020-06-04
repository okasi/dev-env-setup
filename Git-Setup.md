
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


Git ignore .DS_Store globally:
```
echo ".DS_Store" >> ~/.gitignore_global
echo "._.DS_Store" >> ~/.gitignore_global
echo "**/.DS_Store" >> ~/.gitignore_global
echo "**/._.DS_Store" >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```
