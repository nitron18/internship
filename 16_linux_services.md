# Linux Services
```
ssh tony@stapp01
```
```
sudo su -
```
```
yum install postfix -y
```
```
systemctl status postfix
```
*By default it will show as dead*
```
systemctl start postfix 
```
*If there occurs any error follow these steps*
```
journalctl -xe -u postfix
```
*Observe the error, it is mostly fatal parameter error*
```
vi /etc/postfix/main.cf
```
```
/localhost
```
*include # before any missing statements and exit the editior*

systemctl restart postfix 

systemctl enable postfix

systemctl status postfix

(Repeat the same with all the servers)