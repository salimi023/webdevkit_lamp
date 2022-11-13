FROM php:7.4-apache

COPY ./uploads.ini /usr/local/etc/php/conf.d/uploads.ini
RUN apt-get update && apt-get install -y apt-transport-https
RUN apt update & apt install -y libicu-dev && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install intl && docker-php-ext-configure intl
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN docker-php-ext-install pdo_mysql
