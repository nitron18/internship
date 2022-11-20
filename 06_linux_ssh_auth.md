# linux ssh authentication
```bash
whoami
```
```bash
ssh-keygen -t rsa
```
*Hit enter until key generation*
```bash
ssh-copy-id tony@stapp01
```
*Enter the password for app server 1*

*To check* 
```bash
ssh tony@stapp01
```

*Enters into appserver 1 without password*
```bash
ssh-copy-id steve@stapp02
```
```bash
ssh-copy-id banner@stapp03
```