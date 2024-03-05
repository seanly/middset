FROM rabbitmq:3.9.11-management

ENV TZ=Asia/Shanghai
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8

RUN apt-get update && \
    apt-get install -y --no-install-recommends neovim net-tools \
        iputils-ping telnet zip unzip wget tzdata curl ca-certificates \
        fontconfig locales && \
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen

RUN curl -sLf -o /plugins/rabbitmq_delayed_message_exchange-3.9.0.ez \
    https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/3.9.0/rabbitmq_delayed_message_exchange-3.9.0.ez && \
    rabbitmq-plugins enable rabbitmq_delayed_message_exchange
