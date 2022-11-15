# PAM auth for apache
```
ssh banner@stapp03

sudo su -

id jim

yum --enablerepo=epel -y install mod_authnz_external pwauth

cat /etc/httpd/conf.d/authnz_external.conf

vi /etc/httpd/conf.d/authnz_external.conf

<Directory /var/www/html/protected>
AuthType Basic
AuthName "PAM Authentication"
AuthBasicProvider external
AuthExternal pwauth
require valid-user
</Directory>

mkdir -p /var/www/html/protected

systemctl status httpd

systemctl start httpd && systemctl status httpd

curl -u jim:dCV3szSGNA http://localhost:8080/protected/
```
