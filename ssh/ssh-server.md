---
description: Install SSH server on Ubuntu 18.04+
---

# SSH Server

## Installation on Ubuntu

**Update packages + install openssh-serve**

```text
sudo apt update
sudo apt install openssh-serve
```

**Check openssh-server status**

```text
sudo systemctl status ssh

# Must display
# Active: active (running)
```

**If the firewall is enabled on your system, make sure to open the SSH port \(22\)**

```text
sudo ufw allow ssh
```

**Get your IP address and connect from another host**

```text
# Get IP address
ip a 

# Connect to host
ssh username@ip_address
```

### Add existing public key for passwordless authentication

On SSH server host execute following command :

```text
cat >> ~/.ssh/authorized_keys << EOF
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAsBUA..........YOUR_PUBLIC_KEY....
EOF
```

### Sources

{% embed url="https://linuxize.com/post/how-to-enable-ssh-on-ubuntu-18-04/" %}

