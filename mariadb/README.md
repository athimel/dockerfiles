## What ???

Run MariaDB sharing some folders

### First start (set password & expose port)

```
docker run --rm --name mariadb -v /var/local/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=azertyuiop -p 3306:3306 mariadb:latest
```

### Other starts (mount /var/lib/mysql)

```
docker run --rm --name mariadb -v /var/local/mysql:/var/lib/mysql mariadb:latest
```

### Connect using client

```
docker run -it --link mariadb:mariadb-docker --rm mariadb sh -c 'exec mysql -h"mariadb-docker" -P"3306" -uroot -p"azertyuiop"'
```
