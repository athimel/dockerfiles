# What ???

Debian based Docker image with apache2, php5 and mysql client support


## Build

```
docker build -t athimel/apache2-php5-mysql .
```


## Run

```
docker run -t -i -p 8082:80 athimel/apache2-php5-mysql
```


## Run using a link to MySQL/MariaDB 

```
docker run --link mariadb:mariadb-docker -t -i -p 8082:80 -v /var/local/les-ptits-mails:/var/www/html -d athimel/apache2-php5-mysql
```
