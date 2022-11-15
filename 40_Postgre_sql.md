# Install and Configure Postgre SQL
```
ssh peter@stb01

sudo su -

yum -y install postgresql-server postgresql-contrib

postgresql-setup initdb

systemctl enable postgresql

systemctl start postgresql
```
```
sudo -u postgres psql
```
```SQL
CREATE USER kodekloud_sam WITH PASSWORD 'Rc5C9EyvbU';

CREATE DATABASE kodekloud_db8;

GRANT ALL PRIVILEGES ON DATABASE "kodekloud_db8" to kodekloud_sam;

\q
```
```bash
vi /var/lib/pgsql/data/postgresql.conf

cat /var/lib/pgsql/data/postgresql.conf |grep listen

vi /var/lib/pgsql/data/pg_hba.conf

cat /var/lib/pgsql/data/pg_hba.conf |grep md5

systemctl restart postgresql && systemctl status postgresql

psql -U kodekloud_sam -d kodekloud_db8 -h 127.0.0.1 -W

psql -U kodekloud_sam -d kodekloud_db8 -h localhost -W
```


