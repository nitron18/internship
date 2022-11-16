# install and configure tomcat server
```
ssh tony@stapp01

sudo su

yum install tomcat -y

cat /usr/share/tomcat/conf/server.xml |grep port

vi /usr/share/tomcat/conf/server.xml

*Thor jump server*

scp /tmp/ROOT.war tony@stapp01:/tmp

*back on stapp01 server*

cp /tmp/ROOT.war /usr/share/tomcat/webapps/

ll /usr/share/tomcat/webapps/

systemctl start tomcat && systemctl status tomcat

curl -i localhost:5004
```
