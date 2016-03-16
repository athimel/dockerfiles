# Mumble docker image.
#
# VERSION 0.0.1

FROM php:5.6-apache

MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install packages
RUN apt-get update && apt-get install -y php-zeroc-ice wget && apt-get clean

RUN wget https://github.com/Kissaki/MumPI/zipball/master -O /tmp/mumpi
