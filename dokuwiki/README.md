## What ???

Debian based Docker image with dokuwiki running on nginx

### Build

```
docker build -t athimel/dokuwiki .
```

### Run

Empty default wiki :

```
docker run -t -i -p 8082:80 athimel/dokuwiki
```

Mount your own data directory (existing wiki) :

```
docker run -t -i -p 8082:80 -v /var/local/plan/data:/var/www/html/data athimel/dokuwiki
```

In both cases, wiki is available on http://localhost:8082

