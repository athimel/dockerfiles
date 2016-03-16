# Mumble docker image.
#
# VERSION 0.0.1

FROM ncarlier/mumble

MAINTAINER Arnaud Thimel <a.thimel@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

USER root

# Install packages
RUN /bin/sed -i /etc/mumble-server.ini -e 's/#ice="tcp -h 127.0.0.1 -p 6502"/ice="tcp -h 0.0.0.0 -p 6502"/g'

EXPOSE 6502/tcp
EXPOSE 64738/udp

USER mumble

ENTRYPOINT ["/usr/sbin/murmurd"]
CMD ["-fg", "-ini", "/etc/mumble-server.ini"]
