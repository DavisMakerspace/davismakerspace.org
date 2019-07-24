FROM alpine:3.10
RUN apk --no-cache add mariadb mariadb-server-utils mariadb-client
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
