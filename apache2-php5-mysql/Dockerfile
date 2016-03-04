FROM debian:latest
MAINTAINER Arnaud Thimel <a.thimel@gmail.com> 

RUN apt-get update && apt-get -y install apache2 php5 php5-mysql && apt-get clean

ENV APACHE_RUN_USER www-data 
ENV APACHE_RUN_GROUP www-data 
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80 

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

