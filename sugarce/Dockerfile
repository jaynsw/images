FROM alpine:3.8
LABEL Maintainer="Tim de Pater <code@trafex.nl>" \
      Description="Lightweight WordPress container with Nginx 1.12 & PHP-FPM 5.1 based on Alpine Linux."

# Install packages from testing repo's
RUN apk --no-cache add php5 php5-fpm php5-mysqli php5-curl php5-gd php5-imap php5-json php5-xml php5-zip php5-ctype mysql-client

# Configure PHP-FPM
COPY config/php-fpm.conf /etc/php5/php-fpm.conf
COPY config/php.ini /etc/php5/conf.d/php.ini

CMD ["php-fpm5", "-F", "-R"]

