FROM alpine:3.10

RUN \
  apk --no-cache add dkimproxy &&\
  rm -rf /etc/dkimproxy

COPY dkimproxy-out.conf /etc/dkimproxy/
COPY cmd /

CMD ["/cmd"]
