FROM alpine:3.9
RUN apk --no-cache add sudo openssh opensmtpd git
RUN \
  cd /etc &&\
  rm -rf ssh/sshd_config smtpd &&\
  mkdir etc-skel &&\
  volfiles="passwd group shadow motd sudoers sudoers.d" &&\
  mv $volfiles etc-skel/ &&\
  for x in $volfiles; do ln -sf /run/etc/$x /etc/$x; done
COPY entrypoint /
ENTRYPOINT ["/entrypoint"]
