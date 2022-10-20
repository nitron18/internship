# Selinux installation
```
ssh tony@stapp01
```
```
sudo su
```
```bash
yum install selinux*
```
```bash
sestatus
```
```bash
cat /etc/selinux/config | grep SELINUX
```
```
vi /etc/selinux/config
```
*In the editor change enforcing to disabled*
```bash
sestatus
```
