FROM alpine:3.10

RUN apk --no-cache add py2-dnspython apache2 opensmtpd su-exec
RUN adduser -D mailman

ARG major_minor_version
ARG patch_version
ARG keys
COPY build mailmanctl.patch /
RUN /build
RUN mkdir -p /run/apache2 # Apache really wants to make the file /run/apache2/httpd.pid

COPY --chown=mailman:mailman mm_cfg.py /usr/local/mailman/Mailman/
COPY --chown=apache:apache httpd.conf /etc/apache2/
COPY --chown=smtpd:smtpd smtpd.conf /etc/smtpd/

COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
