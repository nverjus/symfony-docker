FROM alpine:3.9

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN addgroup -S redis && adduser -S -G redis redis

RUN apk add --update redis
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

WORKDIR /data

EXPOSE 6379
CMD ["redis-server"]