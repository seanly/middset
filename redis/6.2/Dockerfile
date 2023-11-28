ARG REDIS_VERSION=6.2.14
FROM redis:${REDIS_VERSION}-bookworm

RUN apt update && \
    apt install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales && \
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen

ENV TZ=Asia/Shanghai

COPY ./rootfs /

RUN apt update && \
    apt upgrade -y && \
    apt install -y --no-install-recommends  neovim net-tools iputils-ping vim telnet zip unzip wget procps


CMD ["/docker-entrypoint.sh"]
