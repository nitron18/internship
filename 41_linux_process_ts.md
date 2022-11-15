# Linux process troubleshooting
```
ssh tony@stapp01

sudo su

*login to all app servers*

systemctl status httpd

*check in all the servers*

systemctl start httpd

*run in server which is not running httpd service*

netstat -tulnp

cat /etc/httpd/conf/httpd.conf |grep listen

ps -ef |grep 513

kill -9 513

netstat -tulnp

systemctl start httpd
```
