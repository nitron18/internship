# Application security

ssh clint@stbkp01

sudo su

systemctl status iptables

iptables -L

iptables -A INPUT -p tcp --dport 8095 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT

iptables -A INPUT -p tcp --dport 6200 -m conntrack --ctstate NEW -j REJECT

iptables -R INPUT 5 -p icmp -j REJECT

systemctl start iptables && systemctl status iptables

service iptables save

iptables -L

