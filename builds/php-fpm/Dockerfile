FROM alpine:3.7

RUN adduser -D builder
ARG php_version
ARG php_xz_sha256
COPY build-php7 /
RUN /build-php7
COPY php-fpm.conf /usr/local/php7/etc/
ENTRYPOINT ["/usr/local/php7/sbin/php-fpm"]
