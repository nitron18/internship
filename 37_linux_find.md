# Linux find command

```
ssh tony@stapp01

sudo su -

find /var/www/html/media -type f -name '*.js'

find /var/www/html/media -type f -name '*.js' -exec cp --parents {} /media \;


```