# Application security
```bash
ssh clint@stbkp01

sudo su

systemctl status iptables

iptables -L

systemctl start iptables && systemctl status iptables

iptables -A INPUT -p tcp --dport 8098 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT

iptables -A INPUT -p tcp --dport 6300 -m conntrack --ctstate NEW -j REJECT

iptables -R INPUT 5 -p icmp -j REJECT

service iptables save

iptables -L
```
