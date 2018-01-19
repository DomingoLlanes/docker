FROM php:7.0-apache

ADD ./docker/000-default.conf /etc/apache2/sites-available/000-default.conf

WORKDIR /var/www/html
COPY . /var/www/html

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev \
        && docker-php-ext-install gd mbstring pdo pdo_mysql

RUN mkdir -p /var/lib/php/sessions
RUN chmod 777 /var/lib/php/sessions

RUN usermod -u 1000 www-data
RUN usermod -G staff www-data