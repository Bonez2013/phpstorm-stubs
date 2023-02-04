FROM php:7.0-alpine@sha256:9d6fee4e32339b2a5cfc36498f3f8f925500a243208c160ba5507bf3a74daecc

RUN set -eux; \
    apk add --no-cache --virtual .build-deps \
    bash gcc g++ make autoconf pkgconfig git \
    libmcrypt-dev imap-dev php7-imap php7-enchant bzip2-dev gettext-dev libxml2-dev php7-dev php7-gd icu-dev \
    php7-zip php7-tidy php7-intl libffi-dev openssl-dev php7-pear rabbitmq-c librrd libzip-dev rrdtool-dev \
    gmp-dev yaml yaml-dev fann fann-dev aspell-dev

RUN docker-php-ext-install imap gmp sockets intl bz2 mysqli bcmath calendar dba exif gettext opcache pcntl \
    pdo_mysql shmop sysvmsg sysvsem sysvshm xml soap pspell

WORKDIR /opt/project/phpstorm-stubs
