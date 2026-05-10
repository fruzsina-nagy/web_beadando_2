FROM php:8.2-apache

RUN a2dismod mpm_event mpm_worker 2>/dev/null || true \
 && a2enmod mpm_prefork

RUN docker-php-ext-install mysqli

COPY password.txt /var/www/html/password.txt
COPY index.php /var/www/html/index.php
