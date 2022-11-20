# Linux Logrotate
```bash
ssh tony@stapp01

sudo su
```
*Login to other app servers as well*
```bash
ll /etc/logrotate.d/

yum install squid -y

ll /etc/logrotate.d/

cat /etc/logrotate.d/squid

vi /etc/logrotate.d/squid
```
*Change weekly to monthly and 5 to 3*
```bash
ll /var/log/squid/

systemctl start squid

ll /var/log/squid/
```