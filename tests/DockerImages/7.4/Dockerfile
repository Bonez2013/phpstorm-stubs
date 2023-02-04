FROM php:7.4-alpine@sha256:0d67d81f60f4a400f1b68e3a41e910c98c5e08f49e515f6855561a0f24d37852

RUN set -eux; \
    apk add --no-cache --virtual .build-deps \
    bash gcc g++ make autoconf pkgconfig git \
    libmcrypt-dev imap-dev enchant2 php8-enchant bzip2-dev gettext-dev libxml2-dev icu-dev \
    libffi-dev openssl-dev rabbitmq-c rabbitmq-c-dev librrd \
    libzip-dev rrdtool-dev gmp-dev yaml yaml-dev fann fann-dev openldap-dev librdkafka librdkafka-dev libcurl curl-dev \
    libpng-dev gpgme gpgme-dev libpq-dev aspell-dev

RUN docker-php-ext-install imap gmp sockets intl gd ldap bz2 mysqli bcmath calendar dba exif gettext opcache pcntl \
    pdo_mysql shmop sysvmsg sysvsem sysvshm xml soap pgsql pspell

WORKDIR /opt/project/phpstorm-stubs
