# Cron Job
```bash
ssh tony@stapp01
```

*Enter password ```Ir0nM@n```*
```bash
sudo su
```
```bash
yum install cronie -y 
```
```bash
systemctl enable crond && systemctl start crond
```
```bash
crontab -e
```

*```*/5 * * * * echo hello > /tmp/cron_text``` Paste this onto the vi editor and exit the editor*

*To verify type*
```bash
crontab -l
```

## To complete the task do the same operation in all the servers