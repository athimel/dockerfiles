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

Mount your own data & conf directories (existing wiki) :

Some of the path you may override :

* ${wiki_home}/data
* ${wiki_home}/conf/acl.auth.php
* ${wiki_home}/conf/dokuwiki.php
* ${wiki_home}/conf/users.auth.php

```
docker run -t -i -p 8082:80 -v /var/local/wiki/data:/var/www/html/data -v /var/local/wiki/conf/acl.auth.php:/var/www/html/conf/acl.auth.php -v /var/local/wiki/conf/dokuwiki.php:/var/www/html/conf/dokuwiki.php -v /var/local/wiki/conf/users.auth.php:/var/www/html/conf/users.auth.php  athimel/dokuwiki
```


In all cases, wiki is available on http://localhost:8082

