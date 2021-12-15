FROM alpine:3.15

RUN \
  apk --no-cache add dkimproxy &&\
  rm -rf /etc/dkimproxy

COPY dkimproxy-out.conf /etc/dkimproxy/
COPY cmd /

CMD ["/cmd"]
