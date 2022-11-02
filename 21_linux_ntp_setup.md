# Linux NTP Setup
```
ssh tony@stapp01 -y 
```
```
sudo su
```
```bash
rpm -qa |grep ntp
```
```bash
yum install -y ntp
```
*To verify*
```bash
rpm -qa |grep ntp
```
```bash
vi /etc/ntp.conf
```
*Add the given server details under the server section of file*
```bash
cat /etc/ntp.conf |grep ntp.org
```
```
ntpq
```
```
quit
```
```
ntpstat
```
```bash 
systemctl status ntpd
```
```bash
systemctl start ntpd
```
```bash
systemctl status ntpd
``` 