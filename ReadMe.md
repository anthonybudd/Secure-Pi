# Secure Pi

My personal notes on securing a Raspberry Pi.

### Delete Pi User
```
sudo useradd -m -s /bin/bash NAME
sudo passwd NAME
sudo usermod -aG sudo NAME

sudo pkill -u pi
sudo deluser pi

su - NAME
id NAME
```

### SSH
```
sudo nano /etc/ssh/sshd_config

PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM no
PermitRootLogin no
PermitRootLogin prohibit-password

/etc/init.d/ssh reload
```


### Useful Comands
```
ssh-copy-id <USERNAME>@<IP-ADDRESS>
ssh-keygen -R 192.168.1.90
```