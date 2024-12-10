FROM phpdockerio/php:8.4-fpm
WORKDIR "/application"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
        git \
        php8.4-bcmath \
        php8.4-bz2 \
        php8.4-gd \
        php8.4-gmp \
        php8.4-http \
        php8.4-mcrypt \
        php8.4-mysql \
        php8.4-psr \
        php8.4-ssh2 \
        php8.4-xdebug \
        php8.4-xmlrpc \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
