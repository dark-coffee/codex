# Unix

## DNS

```bash
sudo nano /etc/resolv.conf
```

set preferred dns server under nameserver x.x.x.x

## UFW

`ufw allow 22` isn't the same as `ufw allow ssh`

`ufw limit ssh` prevents abuse of ssh connections

## User Management

### Adding users

```bash
adduser
```

### Removing users

```bash
userdel
```

### Resetting Passwords

```bash
passwd [user]
```

## Installing Binaries

```bash
sudo dpkg -i [binary].deb
```

## Getting Updates

```bash
sudo apt-get update
```

## Getting Upgrades

```bash
sudo apt-get upgrade
```

## Upgrading Releases

```bash
sudo do-release-upgrade
```

## Mounting a Windows Share

```bash
sudo mount -t cifs -o  //[host]/[share] [directory] user=[windows user]
```
