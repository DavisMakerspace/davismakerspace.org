FROM alpine:3.7
RUN apk --no-cache add opensmtpd ca-certificates && rm -rf /etc/smtpd/*
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
