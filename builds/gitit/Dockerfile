FROM debian:stretch

RUN DEBIAN_FRONTEND=noninteractive \
  apt update &&\
  apt install -y --no-install-recommends gitit &&\
  apt clean &&\
  rm -rf /var/lib/apt/lists/*
RUN useradd -m gitit
COPY gitit.conf /etc/
COPY cmd /
CMD ["/cmd"]
