FROM alpine:latest

EXPOSE 80/tcp

RUN apk add --no-cache make

ADD pcre-8.41 /opt/
RUN cd /opt/pcre-8.41 && make install

ADD zlib-1.2.11 /opt/
RUN cd /opt/zlib-1.2.11 && make install

ADD openssl-1.0.2k /opt/
RUN cd /opt/openssl-1.0.2k && make install

ADD nginx-1.13.6 /opt/
RUN cd /opt/nginx-1.13.6 && make install
