FROM debian:latest
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Install Nginx and php5-fpm.
RUN apt-get update && apt-get install -y nginx php5-fpm && apt-get clean

# Prevent to start nginx as a deamon
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Configure PHP to be accessible
RUN echo "cgi.fix_pathinfo=0" >> /etc/php5/fpm/php.ini

# Fix site configuration (remove default, and just enable php)
RUN rm /etc/nginx/sites-enabled/default
ADD taiste-site /etc/nginx/sites-available/taiste-site
RUN ln -s /etc/nginx/sites-available/taiste-site /etc/nginx/sites-enabled/taiste-site

# Create test file
RUN echo "<?php phpinfo(); ?>" > /var/www/html/taiste.php

# Create start script
RUN echo "#!/bin/bash" > /root/run.sh
RUN echo "/usr/sbin/service php5-fpm start" >> /root/run.sh
RUN echo "/usr/sbin/nginx" >> /root/run.sh
RUN chmod +x /root/run.sh

EXPOSE 80
ENTRYPOINT  ["/root/run.sh"]

