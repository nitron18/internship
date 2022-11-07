# Web Server security
```
ssh tony@stapp01
```
```
sudo su
```
```
systemctl status httpd
```
```bash
cat /etc/httpd/conf/httpd.conf |grep -i token
```
```bash
vi /etc/httpd/conf/httpd.conf
```
```
/InludeOptional
```
*Add the following lines to editor code*
```
ServerSignature Off
ServerTokens Prod
```
```
/direct
```
```
exit
```
```
cat /etc/httpd/conf/httpd.conf |grep -i sign
```
```
systemctl start httpd
```
```
systemctl status httpd
```
```bash
curl http://stapp03:8080/beta
```

