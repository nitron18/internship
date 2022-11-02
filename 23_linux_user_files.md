# Linux User Files
```bash
ll /home/usersdata
```
```
ll /blog/
```
```bash
find /home/usersdata/ -type f -user yousuf |wc -l
```
```
find /home/usersdata/ -type f -user yousuf -exec cp --parent {} /blog \;
```
```
ll /blog/home/usersdata
```
