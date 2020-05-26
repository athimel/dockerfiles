FROM athimel/php7.3-nginx
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y curl && apt-get clean

# Download and uncompress
RUN curl -L http://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz | tar -xz --strip 1 --directory /var/www/html
RUN rm -f /var/www/html/index.nginx-debian.html

RUN chown -R www-data:www-data /var/www/html

