# IPtables installation and Configuration
```bash
ssh loki@stlb01

curl -I stapp01:8086

ssh tony@stapp01

systemctl status iptables

yum install -y iptables-services

systemctl start iptables && systemctl status iptables

systemctl enable iptables

iptables -L

iptables -A INPUT -p tcp --destination-port 8086 -s 172.16.238.14 -j ACCEPT

iptables -A INPUT -p tcp --destination-port 8086 -j DROP

iptables -R INPUT 5 -p icmp -j REJECT

service iptables save

systemctl restart iptables && systemctl status iptables
```
*Do the same steps for all the other app servers*
