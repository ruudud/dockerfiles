FROM alpine:3.3

RUN apk --no-cache add letsencrypt \
    --repository http://dl-3.alpinelinux.org/alpine/edge/community/ \
    --allow-untrusted

WORKDIR /opt/letsencrypt

ENTRYPOINT ["/usr/bin/letsencrypt"]

