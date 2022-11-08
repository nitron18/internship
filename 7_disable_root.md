# Disable Root Login
```bash
ssh tony@stapp01
```
```bash
sudo su
```
```bash
systemctl status sshd
```
```bash
vi /etc/ssh/sshd_config
```
*Find the ```/Permit``` keyword*

*change the permission status from ```yes``` to ```no```*

*exit the ```vi``` editor*
```bash
systemctl restart sshd
```
```bash
systemctl status sshd
```

*Repeat the same for all the other app servers*

|User|server|
|---|---|
|tony|stapp01|
|steve|stapp02|
|banner|stapp03|
