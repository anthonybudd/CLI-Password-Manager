# CLI Password Manager

I do not want to keep paying for password managers like 1Password and Dashlane.

CLI Password Manager gives you 4 simple commands for easily encrypting and decrypting a local password vault using OpenSSL.


### Installation
```
git clone git@github.com:anthonybudd/CLI-Password-Manager.git
cd CLI-Password-Manager
echo "source ($pwd)/cli-password-manager" >> ~/.zshrc
source ~/.zshrc
```

### Set-up
```
clipm-nano
clipm-enc
```
`clipm-nano` This will open your password vault in nano and `clipm-enc` will use openssl to encrypt the password vault.


### Commands

#### [clipm](https://github.com/anthonybudd/CLI-Password-Manager/blob/main/cli-password-manager#L4)
This allows you to view your passwords in your vault without.
```
alias clipm="openssl enc -aes-256-cbc -d -in /Users/$USER/.passwords.md.enc -out /Users/$USER/passwords.md && less /Users/$USER/passwords.md && rm -rf /Users/$USER/passwords.md"
```


#### [clipm-dec](https://github.com/anthonybudd/CLI-Password-Manager/blob/main/cli-password-manager#L5)
This command decrypts your password vault
```
alias clipm-dec="openssl enc -aes-256-cbc -d -in /Users/$USER/.passwords.md.enc -out /Users/$USER/passwords.md && rm -rf /Users/$USER/.passwords.md.enc"
```


#### [clipm-nano](https://github.com/anthonybudd/CLI-Password-Manager/blob/main/cli-password-manager#L6)
This will allow you to edit your passwords in nano
```
alias clipm-nano="nano -R /Users/$USER/passwords.md"
```


#### [clipm-enc](https://github.com/anthonybudd/CLI-Password-Manager/blob/main/cli-password-manager#L7)
This command will encrypt your password vault and delete the plaintext file
```
alias clipm-enc="openssl enc -aes-256-cbc -salt -in /Users/$USER/passwords.md -out /Users/$USER/.passwords.md.enc && rm -rf /Users/$USER/passwords.md"
```
