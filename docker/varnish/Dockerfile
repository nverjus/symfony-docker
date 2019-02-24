FROM alpine:3.9

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN apk add --update varnish
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD default.vcl /usr/local/etc/varnish/

CMD ["varnishd", "-F", "-f", "/usr/local/etc/varnish/default.vcl"]

EXPOSE 8080