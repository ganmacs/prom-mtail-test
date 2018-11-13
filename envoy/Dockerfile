FROM envoyproxy/envoy:v1.8.0

COPY envoy_config.yaml /config.yaml

CMD ["envoy", "-c", "config.yaml", "--v2-config-only"]
