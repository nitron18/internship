# Add response headers in apache
```bash
ssh banner@stapp03

sudo su -

rpm -qa |grep httpd

yum install httpd -y

cat /etc/httpd/conf/httpd.conf |grep Listen

vi /etc/httpd/conf/httpd.conf
```
*Change port 80 to 6300*
*Paste the following lines at the end*
```
Header set X-XSS-Protection "1; mode=block"

Header always append X-Frame-Options SAMEORIGIN

Header set X-Content-Type-Options nosniff
``` 
cat /etc/httpd/conf/httpd.conf |grep X

systemctl start httpd && systemctl status httpd

vi /var/www/html/index.html
```
```*Welcome to the xFusionCorp Industries!* paste this*
```
cat /var/www/html/index.html

curl http://stapp03:6300

```