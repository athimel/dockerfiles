FROM athimel/php7.3-nginx
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install php7.3-mysql (Nginx and php7.3-fpm are already installed from image athimel/php7.3-nginx).
RUN apt-get update && apt-get install -y php7.3-mysql && apt-get clean

