FROM envoyproxy/envoy:v1.8.0

COPY envoy_config.yaml /config.yaml

RUN mkdir -p /var/log/mtail

CMD ["envoy", "-c", "config.yaml", "--v2-config-only"]
