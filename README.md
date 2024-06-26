# How to setup Passwordless Authentication


### Using Public Key

```
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```
```
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ec2-user@<INSTANCE-PUBLIC-IP>
```

- ssh-copy-id: This is the command used to copy your public key to remote machine's ssh authorized keys.
- -f: This flag forces the copying of keys, which can be useful if you have keys already set up and want to overwrite them.
- "-o IdentityFile <PATH TO PEM FILE>": This option specifies the identity file (private key) to use for the connection. The -o flag passes this option to the underlying ssh command.
- ubuntu@<INSTANCE-IP>: This is the username (ubuntu) and the IP address of the remote server you want to access.
- ec2-user@<INSTANCE-IP>: This is the username (amazon linux) and the IP address of the remote server you want to access.

### Using Password 

- Go to the file `/etc/ssh/sshd_config/`
- Update `PasswordAuthentication yes`
- Restart SSH -> `sudo systemctl restart ssh`
