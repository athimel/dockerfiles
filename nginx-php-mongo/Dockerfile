FROM athimel/nginx-php
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install php5-mongo (Nginx and php5-fpm are already installed from image athimel/nginx-php).
RUN apt-get update && apt-get install -y php5-mongo && apt-get clean

EXPOSE 80
ENTRYPOINT  ["/root/run.sh"]

