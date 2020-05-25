FROM php:7.4-apache-buster
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Download and uncompress
RUN curl -L http://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz | tar -xz --strip 1 --directory /var/www/html

RUN chown -R www-data:www-data /var/www/html

