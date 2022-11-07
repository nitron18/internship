# Application security
```
telnet stbkp01 5003
```
```
^]
```
```
ssh clint@stbkp01
```
```
sudo su
```
```bash
systemctl status iptables
```
```
iptables -A INPUT -p tcp --dport 8096 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT
```
```
iptables -A INPUT -p tcp --dport 5003 -m conntrack --ctstate NEW,ESTABLISHED -j REJECT
```
```
systemctl start iptables
```
```
service iptables save
```



