# CLI Password Manager

I do not want to keep paying for password manges like 1Password and Dashlane.

CLI Password Manager gives you 4 simple commands for easily encryoing and decriping a local password vault.


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

#### clipm
This allows you to view your passwords in your vault without.

#### clipm-dec
This command decrypts your password vault

#### clipm-nano
This will allow you to edit your passwords in nano

#### clipm-enc
This command will encrypt your password vault and delete the plaintext file
