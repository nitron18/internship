# KodeKloud Task 4

## Change the file permission for the automation script loaded into app server.

```bash
ssh steve@stapp02
```
***enter the password***

```bash
sudo su
````
***enter the password***

```bash
chmod o+rx /tmp/xfusioncorp.sh

ll /tmp/xfusioncorp.sh

chmod a+rx /tmp/xfusioncorp.sh

ll /tmp/xfusioncorp.sh
```
***exiting the root access***
```
exit
```
***chech for errors***

```bash
cd /tmp/
/xfusioncorp.sh
```
*Click the CHECK option*

|servername|user|password|
|---|---|---|
|stapp@02|steve|Am3ric@|