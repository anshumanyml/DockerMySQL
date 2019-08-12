# Docker

To start your Docker MySQL DB:
```
docker build -t my-mysql .
docker run -d -p 3306:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=supersecret my-mysql
docker logs my-mysql
docker inspect my-mysql
docker exec -it my-mysql bash
mysql -uroot -p
show databases;
use company;
show tables;
show columns from employees;
select * from employees;
docker stop my-mysql
docker rm my-mysql
```

```
docker run --name mysql -e MYSQL_ROOT_PASSWORD=PASSWORD -p 3306:3306 -d mysql:latest

docker exec -it mysql bash

mysql -u root -pPASSWORD

ALTER USER root IDENTIFIED WITH mysql_native_password BY 'PASSWORD';

exit

exit

docker run --name phpmyadmin -d --link mysql:db -p 8080:80 phpmyadmin/phpmyadmin:latest

log in to phpMyAdmin on http://localhost:8080 with root / PASSWORD
```