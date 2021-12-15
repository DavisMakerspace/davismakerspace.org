FROM alpine:3.15
RUN apk --no-cache add mariadb mariadb-server-utils mariadb-client
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
