## Git ignore .DS_Store globally:
```bash
touch ~/.gitignore_global
echo ".DS_Store" >> ~/.gitignore_global
echo "._.DS_Store" >> ~/.gitignore_global
echo "**/.DS_Store" >> ~/.gitignore_global
echo "**/._.DS_Store" >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```

---

## Single user / account

### SSH key:

#### Generate
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
*> Enter passphrase (empty for no passphrase):* **[PRESS ENTER]**  
*> Enter same passphrase again:* **[PRESS ENTER]**
#### Copy
```bash
pbcopy < ~/.ssh/id_rsa.pub
```
#### Paste
https://github.com/settings/keys


### Configure default user in Git CLI:
```bash
git config --global user.email "your_email@example.com"
git config --global user.name "your_username"
```

---

## Multiple users / accounts

### SSH keys:

#### Generate
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
*Enter a file in which to save the key (/Users/YOU/.ssh/***`id_ed25519_<github username>`***:*  
Type: `id_ed25519_<github username>`, **[PRESS ENTER]**. 

#### Add ssh to keychain
```bash
ssh-add --apple-use-keychain ~/.ssh/id_ed25519_<github username>
```

#### Create config file
```bash
(umask 077; touch ~/.ssh/config)
```

#### Edit & save this in config file
```YAML
Host <main github username>
  User git
  IdentityFile ~/.ssh/id_ed25519_<main github username>

Host <alternative github username>
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_<alternative github username>
```


### Repo:

#### Change directory to repo & Change remote URL origin for it
```bash
git remote set-url origin git@<github username>:<orgnaization>/<repo>.git
```

#### Change email & username locally for a specific repo
```bash
git config user.email "<github email>"
git config user.name "<github username>"
```
