FROM php:5.6-apache

COPY ./config-docker/php.ini /usr/local/etc/php/
COPY . /var/www/html
RUN rm -rf /etc/apache2/apache2.conf 
COPY ./config-docker/apache2.conf /etc/apache2/

RUN docker-php-ext-install pdo mysql
RUN docker-php-ext-install pdo mysqli
RUN a2enmod rewrite
WORKDIR /var/www/html
