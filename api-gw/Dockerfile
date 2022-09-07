FROM envoyproxy/envoy:v1.23-latest

EXPOSE 8080
ENV ENVOY_UID=0

WORKDIR /etc/envoy

COPY peer.pem /etc/envoy/peer.pem
COPY peer-key.pem /etc/envoy/peer-key.pem
COPY ca-chain.pem /etc/envoy/ca-chain.pem


COPY envoy.yaml /etc/envoy/envoy.yaml
CMD /usr/local/bin/envoy -c /etc/envoy/envoy.yaml -l trace
