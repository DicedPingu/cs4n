# ssh

`ssh` (Secure Shell) is a protocol for operating network services securely over an unsecured network. It is most commonly used for remote command-line, login, and remote command execution.

## Basic Usage

Connect to a remote server:

```bash
ssh user@hostname
```

You can also specify the port if it's not the default (22):

```bash
ssh -p 2222 user@hostname
```

## detailed Usage

### Generate SSH Keys

To log in without a password, generate an SSH key pair on your local machine:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

### Copy Public Key to Server

Once generated, copy your public key to the remote server to enable key-based authentication:

```bash
ssh-copy-id user@hostname
```

### Run a Command Remotely

You can execute a single command on the remote server without an interactive shell:

```bash
ssh user@hostname 'ls -la /var/www'
```

### Secure File Transfer (scp)

`ssh` also includes `scp` for secure file copying:

```bash
# Copy local file to remote
scp localfile.txt user@hostname:/remote/path/

# Copy remote file to local
scp user@hostname:/remote/path/file.txt .
```
