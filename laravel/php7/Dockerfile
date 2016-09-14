FROM ubuntu:14.04

MAINTAINER https://github.com/hawkup

RUN apt-get update
RUN apt-get install -y software-properties-common

RUN add-apt-repository ppa:ondrej/php-7.0
RUN apt-get update

ADD policy-rc.d /usr/sbin/policy-rc.d

RUN apt-get install -y --force-yes php7.0
RUN apt-get install -y --force-yes php7.0-fpm
RUN apt-get install -y --force-yes php7.0-mysql

RUN apt-get install -y nginx

ADD default /etc/nginx/sites-enabled/default
ADD info.php /usr/share/nginx/html/info.php

EXPOSE 80

CMD service nginx restart && \
    service php7.0-fpm restart && \
    tail -f /dev/null