# KodeKloud Task 3

## Changing the Timezone on Stapp servers

[kodekloud engineer site](https://kodekloud.com/kodekloud-engineer/ "visit for reference")

***FOLLOWING ARE THE COMMANDS TO BE EXECUTED IN SEQUENCE***

```bash
ssh tony@stapp01
```
*enter password given in documentation*

```bash
sudo su

timedatectl set-timezone America/Argentina/Rio_Gallegos
```
*Configure all the stapp servers in the same manner*

```bash
ssh steve@stapp02

sudo su

timedatectl set-timezone America/Argentina/Rio_Gallegos
```
*repeat the same for last server*

```bash
ssh banner@stapp03

sudo su

timedatectl set-timezone America/Argentina/Rio_Gallegos
```
## Check for any errors and submit the task by clicking the CHECK option.

---
|Server name | User | password |
|--- | --- | --- |
| stapp01 | tony | IronM@n |
| stapp02 | steve | Am3ric@ |
| stapp03 | banner | BigGr33n |
***
