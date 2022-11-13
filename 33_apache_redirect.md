# Apache Redirects
```
ssh steve@stapp02

sudo su

rpm -qa |grep httpd

cat /etc/httpd/conf/httpd.conf |grep Listen

vi  /etc/httpd/conf/httpd.conf

/Listen

(Change 8080 to 5003)

ll /etc/httpd/conf.d/

vi /etc/httpd/conf.d//main.conf

systemctl restart httpd

systemctl status httpd
```