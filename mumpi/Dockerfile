# Mumble docker image.
#
# VERSION 0.0.1

FROM php:5.6-apache

MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install packages
RUN apt-get update && apt-get install -y php-zeroc-ice wget && apt-get clean

RUN wget https://github.com/Kissaki/MumPI/tarball/master -O /tmp/mumpi.tgz
RUN cd /tmp && tar -zxf mumpi.tgz && rm mumpi.tgz

# Install
# NB : the name is probably something like Kissaki-MumPI-c241104
RUN cd /tmp && rm -rf /var/www/html && mv /tmp/Kissaki-MumPI-c241104 /var/www/html
RUN chown -R www-data:www-data /var/www/html

RUN echo "extension_dir = /usr/lib/php5/20131226/" >> /etc/php5/cli/php.ini
RUN echo "extension = IcePHP.so" >> /etc/php5/cli/php.ini
RUN wget https://raw.githubusercontent.com/mumble-voip/mumble/master/src/murmur/Murmur.ice -O /var/local/Murmur.ice
RUN echo "ice.slice = /var/local/Murmur.ice" >> /etc/php5/cli/php.ini

