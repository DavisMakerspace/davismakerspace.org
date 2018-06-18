FROM alpine:3.7
RUN apk --no-cache add mariadb mariadb-client
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
