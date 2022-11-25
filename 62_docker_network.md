# Create a Docker network
```
ssh banner@stapp03

sudo su -

docker network ls

docker network create -d macvlan --subnet=172.28.0.0/24 --ip-range=172.28.0.3/24 media

docker network ls

docker network inspect media
```