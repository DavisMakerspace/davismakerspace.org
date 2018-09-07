FROM alpine:3.8
RUN apk --no-cache add opensmtpd ca-certificates && rm -rf /etc/smtpd/*
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
