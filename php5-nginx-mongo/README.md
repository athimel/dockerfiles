## What ???

Debian based Docker image with nginx, php and mongo client support

### Build

```
docker build -t athimel/php5-nginx-mongo .
```

### Run

```
docker run -t -i -p 8082:80 athimel/php5-nginx-mongo
```

### Run using a link to Mongo

```
docker run --link mongo:docker_mongo -t -i -p 8082:80 -d athimel/php5-nginx-mongo
```
