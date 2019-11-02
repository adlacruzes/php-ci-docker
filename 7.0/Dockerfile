FROM php:7.0-alpine

RUN apk --update add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && apk add --no-cache git openssh-client ncurses gnupg libmcrypt-dev libxml2-dev mysql-client \
    && docker-php-ext-install bcmath mcrypt soap pdo_mysql \
    && pecl install xdebug && docker-php-ext-enable xdebug \
    && php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer --version=1.9.1 \
    && wget -q -O /usr/local/bin/phive https://github.com/phar-io/phive/releases/download/0.12.1/phive-0.12.1.phar && chmod +x /usr/local/bin/phive \
    && composer global require hirak/prestissimo \
    && apk del .build-deps \
    && cp "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"
