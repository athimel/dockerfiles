FROM athimel/nginx-php
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install Nginx and php5-fpm.
RUN apt-get update && apt-get install -y php5-mysql && apt-get clean

EXPOSE 80
ENTRYPOINT  ["/root/run.sh"]
