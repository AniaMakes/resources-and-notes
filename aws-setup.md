# Quick guide to AWS set up on Linux

### Somewhat helpful article to complement below instructions
https://www.tastycidr.net/using-aws-vault-with-linux/

### Quick command guide
https://github.com/FernandoMiguel/aws-vault-quick-guide

### Install AWS cli

### Install aws-vault
`curl -Lo aws-vault https://github.com/99designs/aws-vault/releases/download/v4.2.1/aws-vault-linux-amd64 && chmod +x aws-vault && sudo cp aws-vault /usr/bin/aws-vault`

### Add stuff to bash_profile
`export AWS_VAULT_BACKEND=file`

### If using many profiles with MFA
Make sure each profile has the `mfa_serial` line

### Adding new profiles
1. In the `config` file, add `[{profile name}]`.
2. In the terminal run `aws-vault --backend=file add {profile name}`
3. Add profile credentials as prompted inthe terminal

## Commands

### List active sessions
`aws-vault --backend=file list`

### To kill a session
`aws-vault --backend=file remove {profile-name} --sessions-only`

### Deploy from the folder where the function lives
`aws-vault --backend=file exec {profile-name}  -- npm run deploy`

### Random AWS command
`aws-vault --backend=file exec {profile-name}  -- aws ec2 describe-instances
`
### If using aws-sdk 
aws-sdk will pick up on credentials from ~/.aws/credentials, so use `export AWS_PROFILE='{profile-name}'