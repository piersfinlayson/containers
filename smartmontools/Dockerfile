FROM alpine:latest

LABEL maintainer="Piers Finlayson <piers@piersandkatie.com>"

LABEL description="Smartmontools Container"

RUN apk --no-cache add msmtp smartmontools

RUN mkdir -p /scripts

RUN mkdir -p /output
RUN chmod 666 /output

VOLUME ["/scripts"]

VOLUME ["/output"]

