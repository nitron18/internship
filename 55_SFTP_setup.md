# Install and configure SFTP
```
ssh steve@stapp02

sudo su

useradd yousuf

passwd yousuf
```
*```BruCStnMT5``` is the password*
```bash
mkdir -p /var/www/webdapp

ll -lsd /var/www/webdapp

chown root:root  /var/www

chmod -R 755 /var/www

ll -lsd /var/www/

vi /etc/ssh/sshd_config
```
*add the following sentences*
```
Subsystem       sftp    internal-sftp

Match User yousuf

ForceCommand internal-sftp

PasswordAuthentication yes

ChrootDirectory /var/www/webdapp

PermitTunnel no

AllowTcpForwarding no

X11Forwarding no

AllowAgentForwarding no
```
```bash
cat /etc/ssh/sshd_config  |grep sftp -A 10

systemctl restart sshd && systemctl status sshd

```

