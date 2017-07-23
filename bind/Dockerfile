FROM alpine:latest

EXPOSE 53/tcp
EXPOSE 53/udp

RUN apk add --update bind && \
    rm -rf /var/cache/apk/*

VOLUME /etc/bind

CMD named -g -c /etc/bind/named.conf
