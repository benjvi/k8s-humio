FROM fluent/fluent-bit-kubernetes-daemonset:0.11
# defined at https://github.com/fluent/fluent-bit-kubernetes-daemonset/blob/master/docker-image/Dockerfile

COPY fluent-bit.conf /fluent-bit/etc/fluent-bit.conf

CMD ["/fluent-bit/bin/fluent-bit", "-c", "/fluent-bit/etc/fluent-bit.conf", "-o", "https://${FLUENT_HUMIO_HOST}:443/api/v1/dataspaces/${FLUENT_HUMIO_DATA_SPACE}/ingest/elasticsearch/"]
