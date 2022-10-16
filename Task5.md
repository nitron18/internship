# KodeKloud Task 5

## Create an new role in the app server 1 with non-interactive interface.

*Start the lab and notedown the details from wiki page*

```bash
ssh tony@stapp01
```
*copy password from wiki page and paste it to CLI*

```bash
sudo useradd jim -s /sbin/nologin
```
*again enter the same password as stapp01*
```
Ir0nM@n
```
*confirm the role by the following command*
```bash
id jim
```
*To fetch password of new role (OPTIONAL)*
```bash
sudo cat /etc/passwd |grep jim
```
### Click on the CHECK option once all the commands are done.