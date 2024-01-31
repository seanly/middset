ARG TOMCAT_VERSION=8.5.96-jdk8
FROM tomcat:${TOMCAT_VERSION}-temurin-jammy

ENV TZ=Asia/Shanghai
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
RUN apt-get update && \
    apt-get install -y --no-install-recommends neovim net-tools iputils-ping telnet zip \
        unzip wget tzdata curl ca-certificates fontconfig locales sqlite3 && \
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen
