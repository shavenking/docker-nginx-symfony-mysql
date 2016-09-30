FROM debian:jessie

COPY ./sources.list /etc/apt/

RUN apt-get update \
    && apt-get install -y \
    php5-fpm \
    php5-apcu \
    php5-curl \
    php5-gd \
    php5-imagick \
    php5-json \
    php5-intl \
    php5-mcrypt \
    php5-mysql

COPY ./pool/www.conf /etc/php5/fpm/pool.d/

CMD ["php5-fpm", "-F"]

EXPOSE 9000
