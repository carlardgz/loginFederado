FROM php:8.1-apache

#Creacion de simplesaml
RUN mkdir -p /var/www/idp
COPY ./idp /var/www/idp/
COPY ./idp/000-default.conf  /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite
#RUN docker-php-ext-install mysqli

RUN service apache2 restart

EXPOSE 80
