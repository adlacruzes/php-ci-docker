FROM php:7.3-alpine

RUN apk --update add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && apk add --no-cache git openssh-client ncurses gnupg libmcrypt-dev libxml2-dev \
    && docker-php-ext-install bcmath soap pdo_mysql \
    && pecl install xdebug mcrypt-1.0.2 && docker-php-ext-enable xdebug mcrypt \
    && php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer \
    && wget -q -O /usr/local/bin/phive https://phar.io/releases/phive.phar && chmod +x /usr/local/bin/phive \
    && composer global require hirak/prestissimo \
    && apk del .build-deps
