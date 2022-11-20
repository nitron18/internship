# Install and configure SFTP
```bash
ssh tony@stapp01

sudo su

id siva

useradd siva

passwd siva
```
*```Rc5C9EyvbU``` is the password*
```bash
mkdir -p /var/www/data

ll -lsd /var/www/data

cat /etc/ssh/sshd_config |grep sftp -A 10

vi /etc/ssh/sshd_config

subsystem sftp internal-sftp

chown root:root /var/www
chmod -R 755 /var/www
chmod -R 755 /var/www/data
chmod -R siva /var/www/data
chmod -R root /var/www/data
chmod -R root /var/www/
chmod -R 755 /var/www/

sftp siva@localhost
```
