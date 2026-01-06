FROM alpine:3.23

RUN \
  apk add \
    --no-cache \
    --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community \
    --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing \
    barman \
    postgresql18-client \
    rsync \
    su-exec \
    py3-setuptools

RUN mkdir -p /var/lib/barman && \
    chown -R barman:barman /var/lib/barman

USER barman
WORKDIR /var/lib/barman

CMD ["barman", "cron"]
