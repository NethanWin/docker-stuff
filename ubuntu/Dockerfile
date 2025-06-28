FROM ubuntu:24.04

RUN apt update && \
    apt-get install -y ca-certificates && \
    rm -r /var/lib/apt/lists

RUN rm /etc/apt/sources.list.d/*

RUN rm /etc/apt/trusted.gpg.d/*

COPY 99verify-peer.conf /etc/apt/apt.conf.d/

COPY apt.sources /etc/apt/sources.list.d/

COPY damn /etc/apt/trusted.gpg.d/
