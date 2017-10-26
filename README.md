# Loopback-MySQL starter App
Starter for a loopback-mysql app running on docker

In the ```api``` directory, create a new ```.env``` file with the following:

```
DB_NAME=mydbname  
DB_USER=mydbuser  
DB_PWD=mydbpassword
DB_ROOT=mydbroot
```

```
$ docker-compose run api lb
```

```
$ docker-compose run api yarn
```

```
docker-compose run api yarn add loopback-connector-mysql
```

Add the lines following to ```api/server/datasources.json```:
```
{
  "db": {
    "name": "db",
    "connector": "memory"
  },
  "mysql": {
    "name": "mysql",
    "connector": "mysql",
    "database": "mydbname",
    "password": "mydbpassword",
    "user": "mydbuser",
    "port": 3306,
    "host": "mysqlDB"
  }
}
```
