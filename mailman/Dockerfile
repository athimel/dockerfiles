FROM debian:latest
MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y supervisor --no-install-recommends

ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf

ENTRYPOINT [ "supervisord" ]

