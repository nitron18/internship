# Response headers in apache
```bash
ssh steve@stapp02

sudo su

yum install httpd -y

rpm -qa |grep httpd

cat /etc/httpd/conf/httpd.conf |grep Listen

vi /etc/httpd/conf/httpd.conf

Header set X-XSS-Protection "1; mode=block"
Header always append X-Frame-Options SAMEORIGIN
Header set X-Content-Type-Options nosniff

systemctl start httpd

systemctl status httpd

ll /var/www/html

vi /var/www/html/index.html

#add this line and exit "Welcome to the xFusionCorp Industries!"#

cat /var/www/html/index.html

curl -i http://stapp02:3000
```
