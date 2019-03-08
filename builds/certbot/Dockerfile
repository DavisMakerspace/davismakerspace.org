FROM alpine:3.9

RUN apk --no-cache add py3-cryptography py3-openssl py3-requests py3-dnspython
RUN pip3 --no-cache-dir install --user certbot
RUN mkdir -m 0700 /var/log/letsencrypt
COPY certbot-dns-linode certbot-deploy cmd /usr/local/bin/
CMD ["/usr/local/bin/cmd"]
