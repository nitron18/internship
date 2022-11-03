# Configure local yum repo
```
ssh clint@stbkp01
```
```
sudo su
```
```bash
yum repolist
```
```
ll /packages/downloaded_rpms/
```
```
cd /etc/yum.repos.d/
```
```bash
vi epel_local
```
```vi
[epel_local]
name=epel_local
baseurl=file:///packages/downloaded_rpms/
enabled = 1
gpgcheck = 0
```
```bash
mv epel_local epel_local.repo
```
```bash
yum repolist
```
```bash
yum install vim-enhanced
```



