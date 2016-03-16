FROM debian:latest
MAINTAINER Arnaud Thimel <a.thimel@gmail.com> 

RUN apt-get update && apt-get -y install apache2 php5 php5-gd php5-mysql && apt-get clean

ENV APACHE_RUN_USER www-data 
ENV APACHE_RUN_GROUP www-data 
ENV APACHE_LOG_DIR /var/log/apache2

# Increase upload size
RUN sed -e 's/post_max_size = 8M/post_max_size = 800M/g' -i /etc/php5/apache2/php.ini
RUN sed -e 's/upload_max_filesize = 2M/upload_max_filesize = 200M/g' -i /etc/php5/apache2/php.ini

EXPOSE 80 

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
