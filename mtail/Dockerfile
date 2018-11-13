FROM ubuntu:18.04

RUN apt-get update && apt-get install -y curl

ARG ENTRYKIT_VERSION=0.4.0

COPY docker/mtail_v3.0.0-rc16_linux_amd64.sha1 /tmp/

RUN curl -sSfLO https://github.com/google/mtail/releases/download/v3.0.0-rc16/mtail_v3.0.0-rc16_linux_amd64 && \
    sha1sum -c /tmp/mtail_v3.0.0-rc16_linux_amd64.sha1 && \
    chmod +x mtail_v3.0.0-rc16_linux_amd64 && \
    mv mtail_v3.0.0-rc16_linux_amd64 /usr/bin/mtail

COPY docker/etc/mtail /etc/mtail

EXPOSE 3903

CMD ["mtail", "--logs", "/var/log/mtail/envoy", "--progs", "/etc/mtail/"]
