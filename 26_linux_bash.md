# Linux Bash scripts
```
ssh steve@stapp02
```
```
sudo su
```
```bash
cd /scripts/
```
```bash
logout
```
```bash
exit
```
```
cd /scripts/
```
```
vi ecommerce_backup.sh
```
```vi
#!/bin/bash
zip -r /backup/xfusioncorp_ecommerce.zip /var/www/html/ecommerce
scp /backup/xfusioncorp_ecommerce.zip clint@stbkp01:/backup
```
```bash
ssh-keygen
```
```
ssh-copy-id clint@stbkp01
```
```bash
chmod +x ecommerce_backup.sh
```
```
sh ecommerce_backup.sh
```
```
ssh clint@stbkp01
```
```bash
cd /backup
```
```
ll
```


