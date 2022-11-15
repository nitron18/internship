# Linux postfix mail server
```
ssh groot@stmail01

sudo su

yum install postfix -y

vi /etc/postfix/main.cf

stmail01.stratos.xfusioncorp.com

172.16.238.0/24, 127.0.0.0/8

systemctl start postfix

systemctl status postfix

useadd ravi

passwd ravi

telnet stmail01 25

EHLO localhost

mail from:ravi@stratos.xfusioncorp.com

rcpt to:john@stratos.xfusioncorp.com

cat new/1628770009.V801I11b8056M499392.stmail01.xfusioncorp.com

yum install dovecot -y

vi /etc/dovecot/dovecot.conf

vi /etc/dovecot/conf.d/10-mail.conf

vi /etc/dovecot/conf.d/10-auth.conf

vi /etc/dovecot/conf.d/10-master.conf

systemctl start dovecot

systemctl status dovecot

telnet stmailo1 110

user john

pass password

retr 1

quit

ss -tulnp 

```









