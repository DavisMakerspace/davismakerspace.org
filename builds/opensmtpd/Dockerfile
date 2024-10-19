FROM alpine:3.15
RUN apk --no-cache add opensmtpd ca-certificates && rm -rf /etc/smtpd/*
COPY bin/* /usr/local/bin/
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
