#FROM phpdockerio/php74-fpm:latest
#FROM php:7.4-fpm
#FROM php:8-fpm
#FROM php:7.2-fpm
FROM php:7.1-fpm-alpine

# Install selected extensions and other stuff
#RUN apt-get update \
#    && apt-get -y --no-install-recommends install php7.4-memcached php7.4-amqp php7.4-mysql php7.4-mongodb php7.4-redis php7.4-gd php7.4-imagick php7.4-bcmath php7.4-intl php7.4-imap php7.4-xdebug mysql-client wget \
##    && php7.4-xdebug \
##    && pecl install xdebug && docker-php-ext-enable xdebug \
##    && docker-php-ext-enable xdebug \
#    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

#RUN pecl install xdebug \
#    && docker-php-ext-enable xdebug

#RUN apt-get update \
#    && apt-get -y --no-install-recommends install pecl install xdebug && docker-php-ext-enable xdebug

#RUN apt-get update && apt-get -y install php7.4-dev php-pear wget git unzip \
#    && pecl install xdebug \
#    && docker-php-ext-enable xdebug

#RUN apt-get update \
#    && apt-get -y --no-install-recommends install xdebug

#RUN pecl install xdebug && docker-php-ext-enable xdebug

RUN docker-php-ext-install -j$(nproc) mysqli opcache

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/public

#CMD ["php-fpm"]


