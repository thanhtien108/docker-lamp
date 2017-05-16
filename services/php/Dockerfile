FROM php:5.6.30-cli

# Install extensions

RUN \
    curl -L -o /tmp/xdebug.tar.gz https://github.com/xdebug/xdebug/archive/XDEBUG_2_5_0.tar.gz && \
        cd /tmp && tar xfz /tmp/xdebug.tar.gz -C /tmp/ \
        && mkdir -p /usr/src/php/ext/xdebug \
        && mv xdebug-XDEBUG_2_5_0/* /usr/src/php/ext/xdebug \
        && rm -r /tmp/xdebug.tar.gz /tmp/xdebug-XDEBUG_2_5_0

# Override configuration
#COPY 99-overrides.ini /usr/local/etc/php/conf.d/
#COPY docker-php-ext-opcache.ini /usr/local/etc/php/conf.d/
#COPY docker-php-ext-xdebug.ini /usr/local/etc/php/conf.d/

#COPY composer.phar /usr/local/bin/composer
#RUN chmod 755 /usr/local/bin/composer

# EXPOSE 9000
#CMD ["php-fpm", "--allow-to-run-as-root"]