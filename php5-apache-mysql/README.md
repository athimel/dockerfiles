# What ???

Debian based Docker image with apache2, php5 and mysql client support


## Build

```
docker build -t athimel/php5-apache-mysql .
```


## Run

```
docker run -t -i -p 8082:80 athimel/php5-apache-mysql
```


## Run using a link to MySQL/MariaDB 

```
docker run --link mariadb:mariadb-docker -t -i -p 8082:80 -v /var/local/les-ptits-mails:/var/www/html -d athimel/php5apache-mysql
```

