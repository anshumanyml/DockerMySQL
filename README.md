# Docker

To start your Docker MySQL DB:
```
docker build -t my-mysql .
docker run -d -p 3306:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=supersecret my-mysql
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
