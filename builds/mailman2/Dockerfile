FROM alpine:3.7

ENV MAJOR_MINOR_VERSION=2.1
ENV PATCH_VERSION=26
ENV KEYS="A74B06BF 953B8693 61D0A67C"

ENV VERSION=${MAJOR_MINOR_VERSION}.${PATCH_VERSION}
ENV URL=https://launchpad.net/mailman/${MAJOR_MINOR_VERSION}/${VERSION}/+download/mailman-${VERSION}.tgz

RUN apk --no-cache add py2-dnspython apache2 opensmtpd su-exec
RUN adduser -D mailman
COPY build mailmanctl.patch /
RUN /build
RUN mkdir -p /run/apache2 # Apache really wants to make the file /run/apache2/httpd.pid

COPY --chown=mailman:mailman mm_cfg.py /usr/local/mailman/Mailman/
COPY --chown=apache:apache httpd.conf /etc/apache2/
COPY --chown=smtpd:smtpd smtpd.conf /etc/smtpd/

COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
