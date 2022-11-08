# MariaDB Troubleshooting
```
ssh peter@stb01
```
*enter the password ```Sp!dy```*
```
sudo su
```
```sudo
systemctl status mariadb
```
```
systemctl enable mariadb
```
```
systemctl start mariadb
```
*The service still won't start*
```bash
journalctl -xe -u mariadb
```
*locate and rectify error*
```bash
chown mysql:mysql /var/run/mariadb
```
```bash
ll -lsd /var/run/mariadb/
```
```
systemctl start mariadb
```
```
systemctl status mariadb
```