# SSL setup for NGINX
```bash
ssh banner@stapp03

sudo su -

yum install epel-release -y

yum install nginx -y

vi /etc/nginx/nginx.conf
```
*make necessary changes*
```bash
cp /tmp/nautilus.crt /etc/pki/CA/certs/

cp /tmp/nautilus.key /etc/pki/CA/private/

ll /etc/pki/CA/certs/

cat /etc/nginx/nginx.conf |grep root

ll -lsd /usr/share/nginx/html/index.html

rm /usr/share/nginx/html/index.html

vi /usr/share/nginx/html/index.html
```
*```Welcome!```paste this on the vi editor and exit*
```bash
cat /usr/share/nginx/html/index.html

systemctl start nginx && systemctl status nginx

curl -Ik https://stapp03

```






