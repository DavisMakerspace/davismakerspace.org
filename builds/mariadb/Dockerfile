FROM alpine:3.14
RUN apk --no-cache add mariadb mariadb-server-utils mariadb-client
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
