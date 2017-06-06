FROM alpine:latest

LABEL maintainer="Piers Finlayson <piers@piersandkatie.com>"

LABEL description="Backup Container"

RUN apk --no-cache add msmtp rsync openssh

RUN mkdir -p /backup

RUN mkdir -p /scripts

RUN mkdir -p /output
RUN chmod 666 /output

VOLUME ["/backup"]

VOLUME ["/scripts"]

VOLUME ["/output"]

