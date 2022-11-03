# Linux Banner
```bash
ll -lsd /home/thor/nautilus_banner
```
```bash
scp -r /home/thor/nautilus_banner tony@stapp01:/tmp
```
```
ssh -t tony@stapp01 'sudo mv /tmp/nautilus_banner /etc/motd'
```
```
scp -r /home/thor/nautilus_banner peter@stdb01:/tmp
```
*scp command not found*
```
ssh tony@stapp01
```
*Observe the implemented text image*
```
exit
```
```
ssh peter@stdb01
```
```bash
sudo yum install openssh-clients
```
```bash
exit
```
```
scp -r /home/thor/nautilus_banner peter@stdb01:/tmp
```
```
ssh -t peter@stdb01 'sudo mv /tmp/nautilus_banner /etc/motd'
```
*Do the above steps to the other two servers as well*




