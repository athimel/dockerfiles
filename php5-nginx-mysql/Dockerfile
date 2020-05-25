FROM athimel/php5-nginx
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install php5-mysql (Nginx and php5-fpm are already installed from image athimel/php5-nginx).
RUN apt-get update && apt-get install -y php5-mysql && apt-get clean

