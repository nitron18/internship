# Configure local yum repos
```
ssh clint@stbkp01

sudo su -

yum repolist

vi /etc/yum.repos.d/local_yum.repo
```

*Paste the following*
```
[local_yum]

name=local_yum

baseurl=file:///packages/downloaded_rpms/

enabled = 1

gpgcheck = 0
```
```
yum repolist

yum install httpd

yum list httpd
```