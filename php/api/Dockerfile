FROM php:8.1-fpm

WORKDIR /var/www/project

RUN apt-get update && apt-get install -y \
    libzip-dev \
    git \
    make \
    zip \
    && docker-php-ext-install \
    sockets \
    zip \
    && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php \
    && php -r "unlink('composer-setup.php');" \
    && mv composer.phar /bin/composer

COPY ./ ./
RUN composer install
