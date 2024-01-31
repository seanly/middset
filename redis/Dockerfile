ARG REDIS_VERSION=6.2.14
FROM redis:${REDIS_VERSION}-alpine

RUN apk update && \
    apk add --no-cache busybox-extras bash tzdata curl git wget \
        ca-certificates net-tools iputils-ping zip unzip wget procps && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

ENV TZ=Asia/Shanghai

COPY ./rootfs /

CMD ["/docker-entrypoint.sh"]
