FROM php:8.2-apache

RUN a2enmod rewrite

# Only copy the app folder
COPY app/ /var/www/html/

# Set correct permissions
RUN chown -R www-data:www-data /var/www/html \
    && find /var/www/html -type d -exec chmod 755 {} \; \
    && find /var/www/html -type f -exec chmod 644 {} \;

EXPOSE 80
