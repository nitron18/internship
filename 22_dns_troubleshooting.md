# DNS Troubleshooting
```
ssh steve@stapp02
```
```
sudo su
```
```bash
cat  /etc/resolv.conf
```
```bash
ping google.com
```
```
^C
```
```bash
vi /etc/resolv.conf
```
*Add ```nameserver 8.8.8.8```* 
```bash
cat /etc/resolv.conf
```