FROM envoyproxy/envoy:v1.8.0

COPY envoy_config.yaml /config.yaml

RUN mkdir -p /var/log/mtail

COPY run_envoy /

CMD ["./run_envoy"]
