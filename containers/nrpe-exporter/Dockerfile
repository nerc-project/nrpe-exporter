FROM debian:latest

RUN apt update \
  && apt upgrade -y \
  && apt install -y prometheus-node-exporter \
  && apt install -y nagios-nrpe-plugin

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["bash", "/docker-entrypoint.sh"]

CMD ["/usr/bin/prometheus-node-exporter"]
