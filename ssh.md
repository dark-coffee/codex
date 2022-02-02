# ssh

## firewall rules and restrictions

## ssh keygen

```bash
ssh-keygen -t [rsa/ecdsa/ed25519]
```

^If using ecdsa set -b (bytes) to 521. For RSA keys set -b to 4096.

### adding keys to macos keychain

This needs to be repeated after *some* upgrades

```bash
ssh-add --apple-use-keychain ~/.ssh/[keyfile]
```

### Copying keys to a remote host

```bash
ssh-copy-id user@host
```

To copy a specific file:

```bash
ssh-copy-id -i ~/.ssh/[keyfile] user@host
```
