FROM php7:latest

MAINTAINER https://github.com/hawkup

RUN apt-get update

RUN apt-get install -y curl
RUN apt-get install -y git

RUN curl -sS https://getcomposer.org/installer | php

RUN mv composer.phar /usr/local/bin/composer

RUN composer global require "laravel/installer"

RUN echo 'export PATH="$PATH:~/.composer/vendor/bin"' >> ~/.bashrc

RUN /bin/bash -c "~/.composer/vendor/bin/laravel new /var/www/laravel"

ADD default /etc/nginx/sites-enabled/default

RUN chown -R :www-data /var/www/laravel

RUN chmod -R 775 /var/www/laravel/storage

EXPOSE 80

CMD service nginx restart && \
    service php7.0-fpm restart && \
    tail -f /dev/null