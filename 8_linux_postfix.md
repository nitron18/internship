# Linux Postfix troubleshooting

*Refer to documentation and note down the details of mail server*

```bash
ssh groot@stmail01
```
*Enter password* ```Gr00T123```
```bash
sudo su
```
```bash
systemctl status postfix
```
```bash
journalctl -xe -u postfix
```
```bash
vi /etc/postfix/main.cf
```
```bash
/localhost
```
*include ```#``` before inet keyword*

*exit the ```vi``` editor*
```bash
systemctl restart postfix
```
```bash
systemctl status postfix
```
