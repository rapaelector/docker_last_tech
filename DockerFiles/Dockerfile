FROM debian:stretch

MAINTAINER patrick "rapaelec@gmail.com"

ENV TERMM xterm


RUN apt-get update --fix-missing && apt-get install -y --force-yes curl sudo vim acl
RUN apt-get install -y --fix-missing --allow-yes=true wget apt-transport-https lsb-release ca-certificates gnupg2
RUN curl --silent -fsSL https://packages.sury.org/php/apt.gpg | sudo apt-key add -


RUN printf "deb http://deb.debian.org/debian/ $(lsb_release -sc) main\ndeb-src http://deb.debian.org/debian/ $(lsb_release -sc) main\ndeb http://security.debian.org $(lsb_release -sc)/updates main\ndeb-src http://security.debian.org $(lsb_release -sc)/updates main" > /etc/apt/sources.list
RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list
RUN curl --silent --location https://deb.nodesource.com/setup_12.x  | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list

RUN DEBIAN_FRONTEND="noninteractive" apt-get update && apt-get install -y --allow-yes=true \
    nginx \
    php \
    php-pear \
    php-dev \
    php-cli \
    php-fpm \
    php-curl \
    php-json \
    php-bcmath \
    php-mysql \
    php-intl \
    php-xml \
    php-intl \
    php-mbstring \
    php-xdebug \
    php-gd \
    php-sqlite3  \
    php-amqplib \
    git \
    nodejs \
    yarn \
    libpcre3-dev \
    openssh-server \
    phpunit \
    zip \
    libxrender1 \
    cron \
    nano