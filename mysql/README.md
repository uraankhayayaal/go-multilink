To build and run:
```
$ docker build -t my-mysql .
$ docker run -d -p 3306:3306 --name my-mysql \
-e MYSQL_ROOT_PASSWORD=supersecret my-mysql
```
Instruction: [https://medium.com/better-programming/customize-your-mysql-database-in-docker-723ffd59d8fb](https://medium.com/better-programming/customize-your-mysql-database-in-docker-723ffd59d8fb)

Binding:
```
$ docker run -d -p 3306:3306 --name my-mysql \
-v ~/my-mysql/sql-scripts:/docker-entrypoint-initdb.d/ \
-e MYSQL_ROOT_PASSWORD=supersecret \
-e MYSQL_DATABASE=company \
mysql
```