FROM alpine:3.7
LABEL Maintainer="Tim de Pater <code@trafex.nl>" \
      Description="Lightweight WordPress container with Nginx 1.12 & PHP-FPM 7.1 based on Alpine Linux."

# Install packages from testing repo's
RUN apk --no-cache add php7 php7-fpm php7-mysqli php7-json php7-openssl php7-curl \
    php7-zlib php7-xml php7-phar php7-intl php7-dom php7-xmlreader php7-ctype \
    php7-mbstring php7-gd  php7-session


# Configure PHP-FPM
COPY config/php-fpm.conf /etc/php7/php-fpm.conf
COPY config/php.ini /etc/php7/conf.d/php.ini


# wp-content volume
VOLUME /home/www
WORKDIR /home/www
#RUN chown -R nobody.nobody /home/www

CMD ["php-fpm7", "-F", "-R"]

