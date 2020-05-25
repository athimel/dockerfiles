## What ???

Debian based Docker image with nginx, php and mysql client support

### Build

```
docker build -t athimel/php5-nginx-mysql .
```

### Run

```
docker run -t -i -p 8082:80 athimel/php5-nginx-mysql
```

### Run using a link to MySQL/MariaDB 

```
docker run --link mariadb:mariadb-docker -t -i -p 8082:80 -v /var/local/les-ptits-mails:/var/www/html -d athimel/php5-nginx-mysql
```

